Refer below examples:

The network address of IPv4 address 192.168.10.117 with the default Class C subnet mask 255.255.255.0 is, 192.168.10.0.

The directed broadcast address of IPv4 address 192.168.10.117 with the default Class C subnet mask 255.255.255.0 is, 192.168.10.255.

The network address of IPv4 address 172.22.18.201 with the default Class B subnet mask 255.255.0.0 is, 172.22.0.0

The directed broadcast address of IPv4 address 172.22.18.201 with the default Class B subnet mask 255.255.0.0 is, 172.22.255.255

The network address of IPv4 address 10.2.122.17 with the default Class A subnet mask 255.0.0.0 is, 10.0.0.0

The directed broadcast address of IPv4 address 10.2.122.17 with the default Class A subnet mask 255.0.0.0 is, 10.255.255.255

But the IPv4 addresses mentioned above are unsubnetted classful IPv4 addresses.

What is the network address of 172.25.191.182 with a subnet mask of 255.255.224.0 ? Now it is started getting difficult.

As a beginner in networking and network security, take some time to learn the below facts.

• If all the bits in the host part are "0", that represents the network address.

• If all the bits in the host part are "0" except the last bit, it is the first usable IPv4 address.

• If all the bits in the host part are "1" except the last bit, it is the last usable IPv4 address.

• If all the bits in the host part are "1", that represents the directed broadcast address.

Question 1 - Find the network address and the directed broadcast address of subnetted Class B IPv4 address 172.25.171.182 with a subnet mask of 255.255.224.0.

Answer: The subnet mask mentioned in above question (255.255.224.0) is not the default Class B subnet mask. The subnet mask 255.255.224.0 can also be represented in <b>CIDR format</b><br> <b>"/19" ( 8+8+3 binary bits in network part)</b
>. Means that, first 19 bits of the IPv4 address belongs to the Network part and remaining 13 bits belongs to the host part.

