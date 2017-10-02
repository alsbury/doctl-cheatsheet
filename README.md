# Digital Ocean Command Line Tool Cheat Sheet
This is a work in progress as I learn how to make use of the tool.

## Compute

### Droplet

`doctl compute droplet create test --size 1gb --image debian-8-x64 --region nyc1 --ssh-keys 4d:23:e6:e4:8c:17:d2:cf:89:47:36:b5:c7:33:40:4e --enable-backups`

### Domains
List domains
`doctl compute domain list`

List records for a domain:
`doctl compute domain records list <mydomain.name>`

*Create A Record*
doctl compute domain records create startchurch.me --record-type "A" --record-name "subdomain_name" --record-data "xxx.xxx.xxx.xxx"

*Create CNAME Record*
doctl compute domain records create startchurch.me --record-type "CNAME" --record-name "subdomain_name" --record-data "domain_name_with_trailing_period"

### Images
