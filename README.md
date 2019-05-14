## Installation

```bash
git clone https://github.com/dmarych/waf-master.git
cd waf-master
vagrant plugin install vagrant-hostmanager
vagrant up
```

## To add records, please use:
```bash
curl -X PUT -d '{"ID":"ip-api1","Name":"ip-api","Address":"ip-api.com","Port":80,"Tags":["test"]}' docker.waf:8500/v1/agent/service/register
```

This setting will create URL like this which can be accessed from your PC:
``` bash
curl http://docker.waf/ip-api
```

## Consul - Dashboard

http://docker.waf:8500/

## Roles
- Consul - deploys and runs Consul container
- Nginx-Proxy - builds and runs Nginx proxy container with Consul-Template included
