# Service Type
***
Originally named TOS (Type of Service), this defines *how the datagram should be handled.*

### Interpretation
***
![[Pasted image 20210904144905.png]]
1. The first 6 bits are **codepoint**
2. The last 2 bits are not used

##### codepoint
The codepoint can be used in 2 different ways.
1. When the 3 right-most bits are 0s,
	- The 3 left most bits are interpreted as the same as the precedence bits. 
	- Compatible with the old interpretation
	- Priority 0-7
		- Low priority Datagrams get discarded first in the case of a router getting congested.
		- For example, a datagram used for network management is much more urgent and important than a datagram containing optional information for a group.
2.  When they are not all 0s,
	- 56 services (64 - 8) are defined with the 6 bits.
	- ![[Pasted image 20210904145650.png]]
		- The first category has 24 services and the rest have 16 each.
			- Category 1 is for Internet Authorities IETF
			- Category 2 is for Local Authorities
			- The third is for experimental purposes  