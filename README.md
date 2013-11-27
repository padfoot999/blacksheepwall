blacksheepwall
===

blacksheepwall is a hostname reconnaissance tool written in Go. 

```
  $ blacksheepwall -h
  Usage: blacksheepwall [options] <ip address or CIDR>

  Options:
  -h, --help            Show Usage and exit.
  -version              Show version and exit.
  -debug                Enable debugging and show errors returned from tasks.
  -concurrency <int>    Max amount of concurrent tasks.    [default: 100]
  -cpus <int>           Max amount of cpus  for the go runtime. [default: 1]
  -server <string>      DNS server address.    [default: "8.8.8.8"]
  -input <string>       Line separated file of networks (CIDR) or
                        IP Addresses.
  -ipv6	                Look for additional AAAA records where applicable.
  -domain <string>      Target domain to use for certain tasks.
  -dictionary <string>  Attempt to retrieve the CNAME and A record for
                        each subdomain in the line separated file.
  -yandex <string>      Provided a Yandex search XML API url. Use the Yandex
                        search 'rhost:' operator to find subdomains of a
                        provided domain..
  -bing	<string>        Provided a base64 encoded API key. Use the Bing search
                        API's 'ip:' operator to lookup hostnames for each host.
  -headers              Perform HTTP(s) requests to each host and look for
                        hostnames in a possible Location header.
  -reverse              Retrieve the PTR for each host.
  -tls                  Attempt to retrieve names from TLS certificates
                        (CommonName and Subject Alternative Name).
  -viewdns              Lookup each host using viewdns.info's Reverse IP
                        Lookup function.
  -fcrdns               Verify results by attempting to retrieve the A or AAAA record for
                        each result previously identified hostname.
  -clean                Print results as unique hostnames for each host.
  -csv                  Print results in csv format.
  -json                 Print results as JSON.

```
