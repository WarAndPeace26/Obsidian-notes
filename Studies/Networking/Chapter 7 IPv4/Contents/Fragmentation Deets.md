# Fragmentation Details
***
The source does not fragment the IP Packet. The transport layer instead segments the data into a size that can be accommodated by IP and the Data Link Layer in use.

When a datagram is fragmented, most of the fields of the datagram headers (Each fragment having a header of its own) are the same. 

The datagrams are independent in which way they'll take to the destination and upon arrival to the destination, they have to be reassembled.

The fields of datagram header that are changed by the router when fragmenting are:
1. [[Flags]]
2. [[Fragmentation Offset]]
3. [[Total length]]