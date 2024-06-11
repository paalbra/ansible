# Wireguard

A relay server should have something like these vars:

```
wireguard_address: "192.168.100.1/24"
wireguard_forward: true
wireguard_peers: [
  {
    name: "test1",
    publickey: "AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA=",
    allowed_ips: "192.168.100.2/32"
  },
  {
    name: "test2",
    publickey: "BBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBB=",
    allowed_ips: "192.168.100.3/32"
  }
]
```

A client should have something like this:

```
wireguard_address: "192.168.100.2/24"
wireguard_peers: [
  {
    name: "server",
    publickey: "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX=",
    allowed_ips: "192.168.100.0/24",
    endpoint: "wg.example.com:51820"
  }
]
```
