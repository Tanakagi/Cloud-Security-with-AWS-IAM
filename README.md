# Cloud-Security-with-AWS-IAM
In this project, I used AWS IAM to create a user, user group, and policy and to secure resource
from having unauthorised access and actions done to my AWS EC2 instances.
- Launch **EC2** instances.
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
 I started this project by Launch EC2 Instances with Tags: <br/>
  <b>I first created my Instances for this project</b>
 <img src="https://i.imgur.com/GLpBWvY.png" height="80%" width="80%" />
<br />
<br />
 I selected, add additional tags which is right next to the Name field, and added a new tag with the following Key and Value.<br/>
        <b>Key = Env<br/>
        <b>Value = production<br/>
<img src="https://i.imgur.com/X4NrErw.png" height="80%" width="80%" />
<br />
<br />
 I choose to proceed without a key pair for Key Pair because this isn’t a long-running instance I will be using.
 Then Clicked  Launch instance. <br/>
 <img src="https://i.imgur.com/7b2RgoZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Then I  created one more EC2 instance for the development environment, where developers can write, test, and debug code before it's deployed to production. And also a live environment that end users can use.  <br/>
<img src="https://i.imgur.com/OoWzpZQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
<br />
I used the same configuration as the previous instance, with the only difference being the tag value for Env.  <br/>
<img src="https://i.imgur.com/5sQdSgi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I then launched the instance.  <br/>
<img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
I then created a new directory named rsadirectory at the root of fileshare1rsa using the portal:  <br/>
<img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I then launched the instance.  <br/>
<img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
I then created a new directory named rsadirectory at the root of fileshare1rsa using the portal:  <br/>
<img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I then launched the instance.  <br/>
<img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
I then created a new directory named rsadirectory at the root of fileshare1rsa using the portal:  <br/>
<img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I then launched the instance.  <br/>
<img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
I then created a new directory named rsadirectory at the root of fileshare1rsa using the portal:  <br/>
<img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I then launched the instance.  <br/>
<img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
I then created a new directory named rsadirectory at the root of fileshare1rsa using the portal:  <br/>
<img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I then launched the instance.  <br/>
<img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
I then created a new directory named rsadirectory at the root of fileshare1rsa using the portal:  <br/>
<img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I then launched the instance.  <br/>
<img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
I then created a new directory named rsadirectory at the root of fileshare1rsa using the portal:  <br/>
<img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I then launched the instance.  <br/>
<img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
I then created a new directory named rsadirectory at the root of fileshare1rsa using the portal:  <br/>
<img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  I then launched the instance.  <br/>
<img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
I then created a new directory named rsadirectory at the root of fileshare1rsa using the portal:  <br/>
<img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  I then launched the instance.  <br/>
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
