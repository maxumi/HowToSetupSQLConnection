# How to connect to VM SQL Server

## Allow Login for SQL Server
1. Download both SQL SERVER and Manager.
2. Login using windows authentication.
3. Click on the Database and choose Properties, then click Security.
4. Under Server  Authentication, choose SQL Server and Windows Authentication mode.
5. Restart the SQL Server
## Allow SQL Server to login with IP address
1. Go to SQL Server Configuration Manager.
2. Open SQL Server Network Configuration and choose Protocols.
3. Click on properties or doubleclick.
4. Set "Yes" in enabled Field and go to Ip Addresses
5. Scroll down to the bottom and find the IPALL Section
6. clear the TCP Dynamic Ports field in that section and set TCP port to be 1433
7. Restart your server
## Allow Firewall so Access from outside is possible
1. Go to Windows firewall.
2. Go to advanced settings.
3. Go to Indbound Rules and click new rule.
4. Choose Port as the new rule.
5. Choose TCP and choose a specfic port of 1433, the same as Server login.
6. Click, "Allow the connection"
7. Click on all 3(Domain, Private amd Public)
8. Then Give it a name.

## What has been done.
1. I have created a login and made sure the server can login with an user.
2. Made sure that its now possible to change the name of the server to the IP address. To login now, use the name like this. **IPADDRESS,PORT**(192.168.1.1,1433). The Port afterwards always need a comma','.
3. The Firewall now can allow other Pc's from the outside since this is for VMs to connect here by using the Ipaddres like before.
