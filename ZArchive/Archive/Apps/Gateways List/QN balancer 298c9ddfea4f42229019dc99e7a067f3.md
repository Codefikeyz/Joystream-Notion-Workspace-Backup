# QN balancer

URL: https://joystreamstats.live/graphql
All content?: No
Discord contact: l1.media
Hired?: No

Description: Requests to this URL are load balanced, meaning distributed, among available QN endpoints provided by JSG and workers in the DAO.

## Setup

JSS nginx snipped for balanced Joystream QN graphql endpoint

```bash
proxy_next_upstream error timeout invalid_header http_500 http_502 http_503 http_504;
upstream QN {
        server query.joystream.org:443;
        #server orion.l1.media:443; # no proposals / threads?
        #server orion.gleev.xyz:443; # Unauthorized
        #server monitoring.joyutils.org:443; # url mismatch: /query/graphql

        #distribution
        #server  sieemmanodes.com:443;
        #server  dp.0x2bc.com:443;
        #server  joystream-distributor.bwarelabs.com:443;
        #server  joystream.koalva.io:443;
        #server  tiguan08.com:443;

        #storage
        server  joystream.yyagi.cloud:443;
        #server  joystream-storage.bwarelabs.com:443; # CF
        server  storage.0x2bc.com:443;
        server  joystream.name:443;
        server  storage.freakstatic.com:443;
        server  itor.space:443;
        server  sieemmastorage.com:443;
        #server  joystreamstorage.jonnyboy.cloud:443; # SSL: error:14094438:SSL routines:ssl3_read_bytes:tlsv1 alert internal error:SSL alert number 80) while SSL handshaking to upstream, client: 185.220.101.34, server: joystreamstats.live, request: "OPTIONS /graphql HTTP/2.0", upstream: "https://148.113.159.201:443/graphql"
        #server  tomato-joystream.yyagi.cloud:443; # htaccess
        #server  adovrn-joystream.yyagi.cloud:443; # htaccess
}

server {
  listen 443 ssl;
  server_name joystreamstats.live;
  root /var/www/joystreamstats.live;

  location /@apollographql {
    proxy_pass https://QN/@apollographql;
  }
  location /graphql {
    proxy_pass https://QN/graphql;
  }
```

### Pioneer network config

```bash
# Mainnet
REACT_APP_TESTNET_NODE_SOCKET=wss://rpc.joystream.org # JSG
REACT_APP_TESTNET_QUERY_NODE=https://query.joystream.org/graphql # JSG
REACT_APP_TESTNET_QUERY_NODE_SOCKET=wss://query.joystream.org/graphql # JSG
REACT_APP_TESTNET_QUERY_NODE=https://joystreamstats.live/graphql # JSS
REACT_APP_TESTNET_QUERY_NODE_SOCKET=wss://joystreamstats.live/graphql # JSS
```