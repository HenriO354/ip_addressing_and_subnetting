

# PROBLEM 6

# PROBLEM 7


# PROBLEM 8
see video explaining the processus to resolve this problem
<a href="https://www.youtube.com/watch?v=GAB1w69J9tQ" target="blank">

<img src="https://www.youtube.com/watch?v=GAB1w69J9tQ" alt="Custom Subnetting Problems" width="240" height="180" border="10" />
</a>

Number of needed subnets: 3 <br>
usable hosts: 45<br>
Network Addresses: 200.175.14.0<br>

|               |     NID       |  HID  |        |       |          |         |          |
|---------------|---------------|-------|--------|-------|----------|---------|----------|
|               |     8  |   7  |   6   |    5   |   4   |    3     |   2     |  1       |
| Nb hosts      |   256  |  128 |  64   |   32   |  16   |    8     |   4     |  2       |
|               |               |       |        |       |          |         |          |
| borrowed bits |    1   |   2  |   3   |    4   |   5   |    6     |   7     |  8       |
|               |               |       |        |       |          |         |          |
| Nb of subnets |    2   |   4  |   8   |   16   |  32   |   64     |  128    | 256      |
| 2^7+2^6 = 192 |    1   |   1  |   0   |    0   |   0   |    0     |   0     |  0       |

<br>

# Hint: Never borrow the last 2 bits of an address !!!
<br>
Default subnetmask: 255.255.255.0 <br>
Total nb subnets: 4<br>
Total nb host addresses: 64<br>
Nb of usable addresses: 64-2 (network and broadcast address) = 62<br>
Nb of bits borrowed: 2 <br>
Customed subnetmask:255.255.255.192 <br>