# utils
`import "github.com/carousell/Orion/utils"`

* [Overview](#pkg-overview)
* [Imported Packages](#pkg-imports)
* [Index](#pkg-index)

## <a name="pkg-overview">Overview</a>

## <a name="pkg-imports">Imported Packages</a>

- [github.com/newrelic/go-agent](https://godoc.org/github.com/newrelic/go-agent)

## <a name="pkg-index">Index</a>
* [Variables](#pkg-variables)
* [func FinishNRTransaction(ctx context.Context, err error)](#FinishNRTransaction)
* [func GetHostname() string](#GetHostname)
* [func GetNewRelicTransactionFromContext(ctx context.Context) newrelic.Transaction](#GetNewRelicTransactionFromContext)
* [func StartNRTransaction(path string, ctx context.Context, req \*http.Request, w http.ResponseWriter) context.Context](#StartNRTransaction)
* [func StoreNewRelicTransactionToContext(ctx context.Context, t newrelic.Transaction) context.Context](#StoreNewRelicTransactionToContext)

#### <a name="pkg-files">Package files</a>
[documentation.go](./documentation.go) [utils.go](./utils.go) 

## <a name="pkg-variables">Variables</a>
``` go
var (
    // NewRelicApp is the reference for newrelic application
    NewRelicApp newrelic.Application
)
```

## <a name="FinishNRTransaction">func</a> [FinishNRTransaction](./utils.go#L65)
``` go
func FinishNRTransaction(ctx context.Context, err error)
```

## <a name="GetHostname">func</a> [GetHostname](./utils.go#L22)
``` go
func GetHostname() string
```

## <a name="GetNewRelicTransactionFromContext">func</a> [GetNewRelicTransactionFromContext](./utils.go#L31)
``` go
func GetNewRelicTransactionFromContext(ctx context.Context) newrelic.Transaction
```

## <a name="StartNRTransaction">func</a> [StartNRTransaction](./utils.go#L46)
``` go
func StartNRTransaction(path string, ctx context.Context, req *http.Request, w http.ResponseWriter) context.Context
```

## <a name="StoreNewRelicTransactionToContext">func</a> [StoreNewRelicTransactionToContext](./utils.go#L42)
``` go
func StoreNewRelicTransactionToContext(ctx context.Context, t newrelic.Transaction) context.Context
```

- - -
Generated by [godoc2ghmd](https://github.com/GandalfUK/godoc2ghmd)