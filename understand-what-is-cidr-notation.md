# <center>CIDR Notation

A system called Classless Inter-Domain Routing, or CIDR, was developed as an alternative to traditional subnetting. The idea is that you can add a specification in the IP address itself as to the number of significant bits that make up the routing or networking portion.

For example, we could express the idea that the
 
                    IP address 192.168.0.15 
 
 is associated with the netmask 
 
                        255.255.255.0 
 
 by using the CIDR notation 
 
                        192.168.0.15/24
 
 This means that the first 24 bits of the IP address given are considered significant for the network routing.

This allows us some interesting possibilities. We can use these to reference “supernets”. 

In this case, we mean a more inclusive address range that is not possible with a traditional subnet mask. 

For instance, in a class C network, like above, we could not combine the addresses from the     networks 

            192.168.0.0 and 192.168.1.0 

because the netmask for class C addresses is 

                    255.255.255.0.

However, using <b>CIDR notation</b>, we can combine these blocks by referencing this chunk as 192.168.0.0/23. This specifies that there are 23 bits used for the network portion that we are referring to.

So the first network (192.168.0.0) could be represented like this in binary:

                    192.168.0.0

    1100 0000 - 1010 1000 - 0000 0000 - 0000 0000

While the second network (192.168.1.0) would be like this:
                    
                    192.168.1.0

    1100 0000 - 1010 1000 - 0000 0001 - 0000 0000

The CIDR address we specified indicates that the first 23 bits are used for the network block we are referencing. This is equivalent to a netmask of 255.255.254.0, or:

    1111 1111 - 1111 1111 - 1111 1110 - 0000 0000

As you can see, with this block the 24th bit can be either 0 or 1 and it will still match, because the network block only cares about the first 23 digits.

CIDR allows us more control over addressing continuous blocks of IP addresses. This is much more useful than the subnetting we talked about originally.

# <center><b>Conclusion

Hopefully by now, you should have a working understanding of some of the networking implications of the IP protocol. While dealing with this type of networking is not always intuitive, and may be difficult to work with at times, it is important to understand what is going on in order to configure your software and components correctly.

There are various calculators and tools online that will help you understand some of these concepts and get the correct addresses and ranges that you need by typing in certain information. CIDR.xyz provides a translation from decimal-based IP addresses to octets, and lets you visualize different CIDR netmasks.