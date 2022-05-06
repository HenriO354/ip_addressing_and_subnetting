https://erikberg.com/notes/networks.html


#   The network address of 

IPv4 address 

                172.22.18.201 
with the default 
Class B subnet mask 

                255.255.0.0 

is 

                 172.22.0.0
<br>

#   Refer below examples:

The network address of IPv4 address 

                192.168.10.117 
with the default 

        Class C subnet mask 255.255.255.0 
is 

                    192.168.10.0

The directed broadcast address of IPv4 address 

                    192.168.10.117 

with the default 

    Class C subnet mask 255.255.255.0 is
                 192.168.10.255

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