### description
---------
a cat in space, eating a croissant, while starting a revolution.
File: chall.jpg.pcap

### solve
-----
* chall.jpg is transmitted one byte as a time throught the data section of ICMP packets.
```py
from scapy.all import *
pcap_file = "chall.jpg.pcap" 
data = bytearray() 
packets = rdpcap(pcap_file)

for packet in packets:
		data += packet[ICMP].load[-8:] 
		
with open('chall.jpg', "wb") as f
	f.write(data)
```

Flag:
![](../_images/Pasted%20image%2020230424000907.png)