# Flags
![[Pasted image 20210904210048.png]]

When the D bit is 1, Fragmentation is prohibited. If it cannot pass, it will discard and send and ICMP error message to the source.

If the More fragments bit is 1, it means that the current datagram is not the last fragment.