### every packet in every protocol has this structure

![d4e9ecd60fce38ddeb090351c5c96721.png](../../../../_resources/d4e9ecd60fce38ddeb090351c5c96721.png)

&nbsp;

generalised view of packet

┌────────────────────┐  
│ Ethernet Header │ ← MAC addresses(datalink layer)  
├────────────────────┤  
│ IP Header │ ← Source/Destination IP, TTL, Protocol (network layer)  
├────────────────────┤  
│ TCP Header │ ← Ports, Sequence Number, Flags (Transport layer)  
├────────────────────┤  
│ Payload │ ← HTTP request, DNS query, file data, etc. (application layer )   
└────────────────────┘

detailed description about OSI layer

![4308d402490b3dfe84ef36fb6e22272a.png](../../../../_resources/4308d402490b3dfe84ef36fb6e22272a.png)