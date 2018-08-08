# Windmill Lane VFX Network Poller

## Requirements

### Abstract

A system that polls for machines on the local network at a period of **10 seconds** and commits the results to a database.

When queried over http, the system returns an array of machines with matching ports in JSON format.

### Example Query:

```
http://127.0.0.1:8080/?port=443
```

### Example Response:

``` json
[
    {
    "ip": "192.168.1.22",
    "mac": "0F:EA:E9:2E:F7:89",
    "ports": [
        "22",
        "443",
        "111",
        "5560",
        "5566",
        "9000",
        "10010"
        ]
    },
    {
        "ip": "192.168.1.23",
        "mac": "13:50:4A:F5:BB:BE",
        "ports": [
            "22",
            "80",
            "443",
            "555",
            "5120",
            "5900",
            "5988",
            "50000"
        ]
    },
    ..........
]
```

## Required Deliverables

* The logic can be coded in any language.
* Any database can be used.
* The system must be deployable using [Docker](https://www.docker.com/) as either:
    * Single Container .
    * Multiple Container with deployment system (eg. shell script, [docker compose](https://docs.docker.com/compose/), etc).
* Instuctions and documentation in Markdown format.
* Commited to a public git account.

## Optional

* Extra host information.
* Other query types.
* UI / Webpage.
* Setting of the polling period.
* Any other features you deem appropriate.
* Tests.
