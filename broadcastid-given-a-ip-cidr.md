#   <center>Identifying the Network and Broadcast Address of a Subnet
<br>In this lesson, we will attempt to simplify the identification of the Network and Broadcast address using a known IP address, within the network or subnet, and the CIDR or Netmask. In this lesson we will walk you through the terms you need to know, the basic math and some examples.

Terms you need to know:

CIDR: Classless Inter-Domain Routing. Think of it as a replacement for a
Netmask. The CIDR Value is equivalent to the number of on bits in a 32 bit
address going left to right. For example: the CIDR value of 24 means the first
24 bits are turned on and the last 8 bits are turned off:

            11111111.11111111.11111111.00000000. 

(See RFC’s: 1519, 1817, 4632).

Network Address (or Network ID): This is the address that identifies the
subnet of a host.

Broadcast Address: An IP Address that allows information to be sent to all
machines on a given subnet rather than a specific machine. (See RFCs: 826, 919,
922, 947, 1027, 1770, 3021).

Binary: A base 2 numbering system (machine language).

Bitwise AND Operator: Represented by the “&” symbol, the Bitwise AND
Operator returns a one in each bit position if both corresponding bits are one.
Example: x & y = z.

Binary Inversion: In a Binary CIDR or Netmask we are inverting the ones to
zeros and the zeros to ones.

Bitwise OR Operator: Represented by the “|” symbol, the Bitwise OR Operator
returns a 1 in each bit position if one or both corresponding bits are one.

The Steps to identify the Network and Broadcast Address of a Subnet

Convert the IP Address and CIDR (or Netmask) to binary.  If you need
additional help you can try our handy Converting IPv4 to
Decimal and Binary IP Conversion Calculators.

Use a Bitwise AND (IP & CIDR) Operator to return the corresponding
values of the IP and CIDR addresses. This gives you the Network Address
(Network ID)  A simple way to use the Bitwise AND Operator in Binary is
show in the following example:

    IP Address: 192.168.1.15

    CIDR: 24 (Netmask: 255.255.255.0)

    Binary IP Address: 11000000.10101000.00000001.00001111

    Binary CIDR: 11111111.11111111.11111111.00000000

Using the Bitwise AND (&) Operator, compare the Binary IP Address to the
Binary CIDR Address. The result will be the Network Address of the IP Address
we are using:

    Binary IP:
    11000000.10101000.00000001.00001111

    Binary CIDR:
    11111111.11111111.11111111.00000000

    Binary Network:
    11000000.10101000.00000001.00000000

The resultant Network Address is 

    11000000.10101000.00000001.00000000.
Converting this back to the format of an IPv4 Address gives us 

    192.168.1.0

This is our <b>Network Address</b>. Therefore, 

    192.168.1.15 
    belongs to the
    192.168.1.0/24 network.

To get the <b>Broadcast Address </b>we need to do a <b>Binary inversion</b> of <b>the <u>CIDR</u> </b>orNetmask Address.

The inversion of the CIDR Address of

        11111111.11111111.11111111.00000000
becomes:

        00000000.00000000.00000000.11111111.

Now we use the Bitwise OR Operator on the Binary Network Address and the inverted CIDR Address to get the Broadcast address.

Binary Network Address:

        11000000.10101000.00000001.00000000

Inverted Binary CIDR:

        00000000.00000000.00000000.11111111

Binary Broadcast Address:       

        11000000.10101000.00000001.11111111

We now convert 

        11000000.10101000.00000001.11111111 

to IPv4 Decimal octet:

                    192.168.1.255

The Broadcast Address for the 

            192.168.1.0/24 Subnet is 
                    192.168.1.255

Now that you have your feet wet, let’s try a few more.

Identify the Network and Broadcast Addresses for each of the following examples:

10.10.1.97/23
192.168.0.3/25
172.16.5.34/26
192.168.11.17/28

Example one: Convert 10.10.1.97/23 to Binary.

IP Address: 

        00001010.00001010.00000001.01100001

CIDR Address: 

        11111111.11111111.11111110.00000000

Use Bitwise AND Operator (IP & CIDR):

IP Address:

        00001010.00001010.00000001.01100001

CIDR Address:

        11111111.11111111.11111110.00000000

Network Address: 

        00001010.00001010.00000000.00000000

Network Address: 

                    10.10.0.0

Binary Inversion of CIDR:

Binary CIDR:

        11111111.11111111.11111110.00000000

Inverted Binary CIDR:   00000000.00000000.00000001.11111111

Use Bitwise OR Operator to get the Broadcast Address:

Binary Network:    

        00001010.00001010.00000000.00000000

Inverted Binary CIDR:    

        00000000.00000000.00000001.11111111

Binary Broadcast:    

        00001010.00001010.00000001.11111111

Broadcast Address:    

                    10.10.1.255

IP Address 

                    10.10.1.97/23 

belongs to the 

                10.10.0.0/23 Network 

The network Address is 

                    10.10.0.0 

and the Broadcast Address is 

                    10.10.1.255.

Example two: Convert 192.168.0.3/25 to Binary.

IP Address: 

            11000000.10101000.00000000.00000011

CIDR Address: 

            11111111.11111111.11111111.10000000

<center>Use Bitwise AND Operator 

(IP & CIDR)

IP:

        11000000.10101000.00000000.00000011

CIDR:

        11111111.11111111.11111111.10000000

Network:     

        11000000.10101000.00000000.00000000

Network Address: 

            192.168.0.0

<center>Binary Inversion of CIDR:

Binary CIDR:

        11111111.11111111.11111111.10000000

Inverted Binary CIDR:   

        00000000.00000000.00000000.01111111

Use Bitwise OR Operator to get the Broadcast Address:

Binary Network:    

        11000000.10101000.00000000.00000000

Inverted Binary CIDR:    

        00000000.00000000.00000000.01111111

Binary Broadcast:    

        11000000.10101000.00000000.01111111


Broadcast Address:    

        192.168.0.127

IP Address 

        192.168.0.3/25 belongs to the 
        
        192.168.0.0/25 Network. 
        
The network Address is 
        
    192.168.0.0 
and the Broadcast Address is 

    192.168.0.127
</center>
Example three: Convert 192.168.11.17/28 to Binary.
IP Address: 

        11000000.10101000.00001011.00010001

CIDR Address: 

        11111111.11111111.11111111.11110000

Use Bitwise AND Operator (IP & CIDR):



    IP:   11000000.10101000.00001011.00010001

    CIDR: 11111111.11111111.11111111.11110000

    Network:11000000.10101000.00001011.00010000

    Network Address: 192.168.11.16

<center>Binary Inversion of CIDR:


    Binary CIDR:
    11111111.11111111.11111111.11110000

    Inverted Binary CIDR:   00000000.00000000.00000000.00001111

<center>Use Bitwise OR Operator to get the Broadcast Address:

    Binary Network:11000000.10101000.00001011.00010000

     Inverted Binary CIDR:    
        00000000.00000000.00000000.00001111