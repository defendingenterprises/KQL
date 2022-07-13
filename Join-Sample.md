# Sample data for testing of Join operator

```
let DomainMapping = datatable(WorkstationName:string,Domain:string)
[
    "az-wks-05","insecurity.local",
    "az-wks-06","insecurity.local",
    "az-wks-08","defendingenterprises.com",
    "az-wks-08","example.com",
    "az-wks-09","hackingenterprises.com",
];
let SystemMapping = datatable(WorkstationName:string,HostLocalIpAddress:string)
[
    "az-wks-05","192.168.2.5",
    "az-wks-06","192.168.2.6",
    "az-wks-07","192.168.2.7",
    "az-wks-08","192.168.2.8",
];
DomainMapping
| join kind=[REPLACE] SystemMapping on WorkstationName
```
