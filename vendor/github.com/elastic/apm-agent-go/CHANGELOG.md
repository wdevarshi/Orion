# Changelog

## [Unreleased](https://github.com/elastic/apm-agent-go/compare/v0.5.2...master)

 - Implement v2 intake protocol (#180)
 - Unexport Transaction.Timestamp and Span.Timestamp (#207)
 - Add jitter (+/-10%) to backoff on transport error (#212)
 - Add support for span tags (#213)
 - Require units for size configuration (#223)
 - Require units for duration configuration (#211)
 - Add support for multiple server URLs with failover (#233)
 - Add support for mixing OpenTracing spans with native transactions/spans (#235)
 - Drop SetHTTPResponseHeadersSent and SetHTTPResponseFinished methods from Context (#238)
 - Stop setting custom context (gin.handler) in apmgin (#238)
 - Set response context in errors reported by web modules (#238)
 - module/apmredigo: introduce gomodule/redigo instrumentation (#248)
 - Update Sampler interface to take TraceContext (#243)
 - Truncate all strings to a maximum of 10000 chars (#244)
 - Add leading slash to URLs in transaction/span context (#250)
 - Add `Transaction.Context` method for setting framework (#252)
 - Timestamps are now reported as usec since epoch, spans no longer use "start" offset (#257)
 - `ELASTIC_APM_SANITIZE_FIELD_NAMES` and `ELASTIC_APM_IGNORE_URLS` now use wildcard matching (#260)
 - Changed top-level package name to "apm", and canonical import path to "go.elastic.co/apm" (#202)
 - module/apmrestful: introduce emicklei/go-restful instrumentation (#270)
 - Fix panic handling in web instrumentations (#273)

## [v0.5.2](https://github.com/elastic/apm-agent-go/releases/tag/v0.5.2)

 - Fixed premature Span.End() in apmgorm callback, causing a data-race with captured errors (#229)

## [v0.5.1](https://github.com/elastic/apm-agent-go/releases/tag/v0.5.1)

 - Fixed a bug causing error stacktraces and culprit to sometimes not be set (#204)

## [v0.5.0](https://github.com/elastic/apm-agent-go/releases/tag/v0.5.0)

 - `ELASTIC_APM_SERVER_URL` now defaults to "http://localhost:8200" (#122)
 - `Transport.SetUserAgent` method added, enabling the User-Agent to be set programatically (#124)
 - Inlined functions are now properly reported in stacktraces (#127)
 - Support for the experimental metrics API added (#94)
 - module/apmsql: SQL is parsed to generate more useful span names (#129)
 - Basic vgo module added (#136)
 - module/apmhttprouter: added a wrapper type for `httprouter.Router` to simplify adding routes (#140)
 - Add `Transaction.Context` methods for setting user IDs (#144)
 - module/apmgocql: new instrumentation module, providing an observer for gocql (#148)
 - Add `ELASTIC_APM_SERVER_TIMEOUT` config (#157)
 - Add `ELASTIC_APM_IGNORE_URLS` config (#158)
 - module/apmsql: fix a bug preventing errors from being captured (#160)
 - Introduce `Tracer.StartTransactionOptions`, drop variadic args from `Tracer.StartTransaction` (#165)
 - module/apmgorm: introduce GORM instrumentation module (#169, #170)
 - module/apmhttp: record outgoing request URLs in span context (#172)
 - module/apmot: introduce OpenTracing implementation (#173)

## [v0.4.0](https://github.com/elastic/apm-agent-go/releases/tag/v0.4.0)

First release of the Go agent for Elastic APM
