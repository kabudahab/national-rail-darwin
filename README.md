# national-rail-darwin

### Introduction

`national-rail-darwin` aims to give you json object representations of the SOAP responses from National Rail's Darwin api. 

Currently only CRS codes are supported, a future update will allow full station names to be used. You can find a complete list of CRS codes on the [ National Rail website ] (http://www.nationalrail.co.uk/stations_destinations/48541.aspx)

### Installation

```
npm install national-rail-darwin
```

### Usage

Currently 3 of the 11 functions that Darwin exposes are available in `national-rail-darwin`
- getArrivalBoard(crsCode, number of rows, options, callback)
- getDepartureBoard(crsCode, number of rows, options, callback)
- getServiceDetails(serviceId, callback)

```javascript
var rail = require('national-rail-darwin')
rail.getDepartureBoard('LGX', 10, options, function(err,result){
	//do stuff
})

rail.getArrivalsBoard('PUT',10, null, function(err, result){
	//do stuff
})

rail.getServiceDetails('SERVICE ID', function(err, result){
	//do stuff
})
```