**detect the presence on firewall using -sA**

**![d9f0f0cb89ece97b9867c4d7a22932d1.png](../../../images/d9f0f0cb89ece97b9867c4d7a22932d1.png)**

**unfiltered port confirms that their is no firewall at the host**

**filtered ports may tells us that their is a firewall sitting on the host**

&nbsp;

# **IDS evasion**

**with -f option the packets are fragmented during transmission at the network layer.**

**can use --mtu to set custom minimum size of the fragment length**

**![0ef6f59b428a6859a49e0a7bd6a58049.png](../../../images/0ef6f59b428a6859a49e0a7bd6a58049.png)**

**Bypass any manual detection by using decoy ip's (using randomm IP's)**

**![ea8b0589d7b35fb265c03b45442047cf.png](../../../images/ea8b0589d7b35fb265c03b45442047cf.png)**

**The scan also be bypassed by using a well known port like 53 ,that tell the network a DNS request might be coming from a router(by using the gateway IP)**

**![b8898af270f2f3510f498e8ee5b3df76.png](../../../images/b8898af270f2f3510f498e8ee5b3df76.png)**