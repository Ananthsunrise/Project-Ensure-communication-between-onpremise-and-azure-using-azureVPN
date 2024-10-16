# Project-Ensure-communication-between-onpremise-and-azure-using-azureVPN

**Description:**
Azure vpn used to achieve commnunication between onpremise and azure network.
3 catagories: 1.point to site vpn->connect external devices such as laptop,mobile to azure network thorough internet(speed1gbs)
              2.site to site vpn->connect company on prem to azure network through internet(speed1gbps)
              3.express route->connect onpremises to azure network through fiber cable(speed 10gbps)

**Procedure :**
Step 1 : **create vpn gateway**
go to azure portal->search virtual network gateway->click create->select vnet
after creating vpn gateway in azure vnet, gateway subnet is automatically created. no need to create manually.

Step 2: **configure point to site vpn gateway**
Go to azure portal->click the above created vpn gateway->select point to site configuration under settings->give address pole as cidr range(for example:10.0.0.0/22)->select authentication as azure certificate.

Step 3 : **download root certificate and client certificate for azure vpn**
Download both certificated from powershell. you can commands fro internet or chatgpt.
Attach root certificate to azure network
Attach client certificate to local system(laptop)

Step4: **download vpn software in laptop**
go to azure portal->click the above created vpn gateway->click point to site configuration under settings->click download vpn and install it.

Step5 : **Connect vpn in you local system and start login into virtual machine**
              
