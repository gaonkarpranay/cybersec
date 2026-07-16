**FTP Enumeration**  
\> FTP (File Transfer Protocol) is a protocol that uses TCP port 21 and is used to facilitate file sharing between a server and client/clients.  
\> It is also frequently used as a means of transferring files to and from the directory of a web server.  
\> We can use multiple auxiliary modules to enumerate information as well as perform brute-force attacks on targets running an FTP server.  
\> FTP authentication utilizes a username and password combination, however, in some cases an improperly configured FTP server can be logged into  
anonymously.

![9e185fbb96e6d355777b30c08dd4abac.png](../../../../eJPT/images/9e185fbb96e6d355777b30c08dd4abac.png)

**we can search for version module of msf to identify he version of ftp**

**![27a9e37544b15ce837dfd06ff9b490a6.png](../../../../eJPT/images/27a9e37544b15ce837dfd06ff9b490a6.png)**

**we can also use a ftp_login module to try logging to the server using user and password files**

**![18eaa55b994e49fc0ba07672512a8d5e.png](../../../../eJPT/images/18eaa55b994e49fc0ba07672512a8d5e.png)**

**once we have valid credentials for the username and password we can login to the ftp**

**![ae824e7f5650b4e2d916ae6aee922f93.png](../../../../eJPT/images/ae824e7f5650b4e2d916ae6aee922f93.png)192.249.10.3**