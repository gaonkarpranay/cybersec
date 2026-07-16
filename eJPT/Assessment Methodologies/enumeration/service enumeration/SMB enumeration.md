![5e4939493cb79785b348552faa8bb242.png](../../../eJPT/images/5e4939493cb79785b348552faa8bb242.png)

**Nmap scan for the Host**

**![c4bad0f695b00c6c8069b5f8d67b2f4f.png](../../../eJPT/images/c4bad0f695b00c6c8069b5f8d67b2f4f.png)**

&nbsp;

**setting global variable rhost**

![5e1ff8d43576f398c250a3c2831f3e36.png](../../../eJPT/images/5e1ff8d43576f398c250a3c2831f3e36.png)

&nbsp;

**smb version enumeration**

**![467b657e7964efcb6fcc1466ac599f7f.png](../../../eJPT/images/467b657e7964efcb6fcc1466ac599f7f.png)**

&nbsp;

**SMB user enumeration, now we have the user list we can try bruteforcing the password for the users**

**![139cfb506938710dd0dcc90ba076b071.png](../../../eJPT/images/139cfb506938710dd0dcc90ba076b071.png)**

&nbsp;

**Shares enumeration , now we have the shares we can try to access thes shares and find any sensitive files**

**![a3423345d91950844f4835e5994323ea.png](../../../eJPT/images/a3423345d91950844f4835e5994323ea.png)**

&nbsp;

**Password bruteforcing using another module for the user admin**

**![2151926f2ed16b3691f5439b37c88657.png](../../../eJPT/images/2151926f2ed16b3691f5439b37c88657.png)**

&nbsp;

**Now with the user details and share details we can access the shares and eventually access the sensetive files on the shares**

**![00033179b77031bc8c3ad23a30d29cbf.png](../../../eJPT/images/00033179b77031bc8c3ad23a30d29cbf.png)**

&nbsp;

&nbsp;