# Time to Live
***
This field controls **Maximum Number or Hops**.
Each router that processes the Datagram decrements this number by 1. A datagram with a TTL of gets discarded.

##### Uses
***
This field is needed because
- Routing tables often get corrupted and a datagram ends up traveling between two or more routers without ever reaching the destination. This field limits the lifetime of a datagram
- It can also be used to **Intentionally limit the lifetime of a datagram** to keep it confined in, say, the local network (With a TTL of 1).