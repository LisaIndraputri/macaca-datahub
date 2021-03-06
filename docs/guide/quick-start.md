# Quick Start

## Create New Project

Create a new item named sample.

<div align="center">
  <img src="https://ws1.sinaimg.cn/large/796b664dgy1fuueeskabij21yg1bo43p.jpg" width="75%" />
</div>

## Add An Interface

Add the interface named `test1`, request the interface `http://localhost:8080/api/test1` and get the corresponding mock data.

<div align="center">
  <img src="https://ws1.sinaimg.cn/large/796b664dgy1fuueesm0htj21xm1aidla.jpg" width="75%" />
</div>


## Build Interface

The scene management, add scenario content corresponding to Response, and the development environment adds multiple scenarios which is conducive to rapid switching. You cna set the interface response information, and return status code `200` if not set.

<div align="center">
  <img src="https://wx3.sinaimg.cn/large/bceaad1fly1g0fkh7hxmgj218t0u0h59.jpg" width="75%" />
</div>

The proxy pattern, it can be configured if required.

<div align="center">
  <img src="https://ws1.sinaimg.cn/large/796b664dgy1fuueesyt33j21y61ay463.jpg" width="75%" />
</div>

Request field description, you can use scheme JSON for validation and choose whether to open validation or not.

<div align="center">
  <img src="https://ws1.sinaimg.cn/large/796b664dgy1fuueesm12ej21y01aqtew.jpg" width="75%" />
</div>

Response field description, you can use scheme JSON for validation and choose whether to open validation or not. Response descriptions are automatically generated based on scenario information configuration.

<div align="center">
  <img src="https://ws1.sinaimg.cn/large/796b664dgy1fuueesmb50j21xe1bqq94.jpg" width="75%" />
</div>

## Generating Document

Automatically generate documents based on interfaces.

<div align="center">
  <img src="https://ws1.sinaimg.cn/large/796b664dgy1fuueet04ehj21yk1b4gst.jpg" width="75%" />
</div>

## Try Now

Specific code reference [webpack-datahub-sample](//github.com/macaca-sample/webpack-datahub-sample).

```javascript
var request = new XMLHttpRequest();
request.open('GET', '/api/test1', true);

request.onreadystatechange = function() {
  if (this.readyState === 4) {
    if (this.status >= 200 && this.status < 400) {
      var json = JSON.parse(this.responseText);
      document.querySelector('#value').innerHTML = json.data;
    } else {}
  }
};

request.send();
```

The mock data is displayed in the page after requesting the `http://localhost:8080/api/test1` interface.

<div align="center">
  <img src="https://ws1.sinaimg.cn/large/796b664dgy1fuugd10nbyj21t21amq9p.jpg" width="75%" />
</div>


## History Request Information

This page displays historical request details.

<div align="center">
  <img src="https://ws1.sinaimg.cn/large/796b664dgy1fuuewr0rmyj21xu1aytet.jpg" width="75%" />
</div>

