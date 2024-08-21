# Cloud-Security-with-AWS-IAM
In this project, I used AWS to - Launch **EC2** instances.
- Use **tags** for easy identification.
- Set up **IAM policies** accessing EC2 instances based on their environment (development or production).
- Create an **IAM user** and assign them to the appropriate user group with the necessary permissions for their role.
- **Test IAM access** for the User I created.


<h2>AWS Services Used </h2>

- <b>**AWS Portal**</b> 
- <b>**Amazon** **EC2**</b>
- <b>**Amazon** **IAM**</b>  
  
<h2>Project walk-through:</h2>

<p align="center">
 I started this project by using the Azure CLI to create an Azure resource group named datacenterhq1: <br/>
<img src="https://i.imgur.com/GLpBWvY.png" height="80%" width="80%" />
<br />
<br />
I then verified the creation of datacenterhq1 in the portal:  <br/>
<img src="https://i.imgur.com/X4NrErw.png" height="80%" width="80%" />
<br />
<br />
Once the resource group was created I used the CLI to create a storage account named storesyncrsa:  <br/>
 <img src="https://i.imgur.com/7b2RgoZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I then verified the creation of storesyncrsa in the portal:  <br/>
<img src="https://i.imgur.com/OoWzpZQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
<br />
After creating the storage account storesyncrsa, I started the creation of the file share fileshare1rsa:  <br/>
<img src="https://i.imgur.com/5sQdSgi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I verified the creation of the file share fileshare1rsa in the portal.:  <br/>
<img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
I then created a new directory named rsadirectory at the root of fileshare1rsa using the portal:  <br/>
<img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Once the directory was created I then uploaded my local files to it using the portal, which was the last step of this project:  <br/>
<img src="https://i.imgur.com/U0Q7UFL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <img src="https://i.imgur.com/jZvfkiL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
