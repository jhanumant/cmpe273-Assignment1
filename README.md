# cmpe273-Assignment1
# json-rpc-Trading Engine
Example JSON-RPC .

Stock Trading engine using YAHOO API

## Usage
User can know current prices of stocks and can know his investments(desired)
### Install

```
go get github.com/jhanumant/cmpe273-Assignment1
```

Start the  server:

```
cd cmpe273-Assignment1
go run Server.go
```
### Make RPC calls From Client for Buying Stocks

```
cd cmpe273-Assignment1
go run Client.go "stockSymbolAndPercentage":"GOOG:50%,YHOO:50%" "budget":3000
```

```
Response:

"tradeid":2
"stocks":"GOOG:2:$626.91,YHOO:48:$30.71"
"unvestedAmount":272.10
```
### Make RPC calls From Client for Seeing Portfolio
```
go run Client.go "tradeid":2
```

```
Response:

"stocks":"GOOG:2:$626.91,YHOO:48:$30.71"
"currentMarketValue":2727.9
"unvestedAmount":272.10
```

Comments: Run the Server.go file first using "go run Server.go" (without double quotes) and in separate command prompt run the 
client.go along with the arguments specified as an example above
