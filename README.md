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

<p align="left">
 I started this project by Launch EC2 Instances with Tags: <br/>
  <b>I first created my Instances for this project</b>
 <img src="https://github.com/Tanakagi/Cloud-Security-with-AWS-IAM/blob/88ce441e5b1ce7ee19f5121d70bc3262df613f17/Project%20images/image%201.png" height="80%" width="80%" />
<br />
<br />
 I selected, add additional tags which is right next to the Name field, and added a new tag as follows:<br/>
        <b>•Key = Env<br/>
        <b>•Value = production<br/>
 <img src="https://i.imgur.com/X4NrErw.png" height="80%" width="80%" />
<br />
<br />
 I choose to proceed without a key pair for Key Pair because this isn’t a long-running instance I will be using.<br/>
 Then Clicked  Launch instance. <br/>
 <img src="https://i.imgur.com/7b2RgoZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Then I  created one more EC2 instance for the development environment, where developers can write, test, and debug<br/>
          code before it's deployed to production. And also a live environment that end users can use.  <br/>
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
 <h3>Creation of an IAM Policy: I  went to the IAM console page.</h3>
  <b>• On the left-hand navigation panel of the IAM console, choose Policies.<br/>
  <b>• Selected Create policy.<br/>
  <b>• Switch your Policy editor tab to JSON.<br/>
  <b>• I then entered the following Policy which, allows all EC2-related actions that have the<br/>
Environment tag and Development. However, it denies creating and deleting tags for EC2 instances.  <br/>
 <img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
• I then selected next and filled in the policy name and description.  <br/>
 <img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
 • I then selected Create Policy. <br/>
 <img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <h3>The next step was to create an AWS Account Alias</h3>
    <b>• I went to the IAM dashboard.<br/>
    <b>• In the right-hand side of the dashboard, I selected create  under Account Alias.  <br/>
 <img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
 <h3>Create IAM Users and User Groups</h3>
    <b>• I then created my first user group for securityproject-dev-group<br/>
    <b>• and Attached permission policies: SecurityProjectDevEnvironmentPolicy  <br/>
 <img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
• I then launched the instance.  <br/>
 <img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
 <h3>The next step was to create an AWS Account Alias</h3>
     <b>•I went to the IAM dashboard. <br/>
     <b>•In the right-hand side of the dashboard, I selected create  under Account Alias. <br/>
 <img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
• I then created a user to add to my user groups <br/>
 <img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
 <h3>The next step was Testing my user's access</h3>
<b>• I pasted the new console sign-in URL in your incognito window.<br/>
<b>• filled in the information and signed in  <br/>
 <img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 I went to my console, and made sure I was in the same Region as the one where you deployed your two<br/> 
  production and development instances. and tried to stop the Production Instance. <br/>
<img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
 I then got this error message. This happened because the policy I created and attached to the user group that my user was a part of, <br/>
  which only allowed all EC2-related actions to instances with the Env development tag. <br/>
  This instance had the Env production tag, not the Env development tag. <br/>
<img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I then attempted to stop the development instance. and was successful since this instance had the  Env development tag. <br/>
<img src="https://i.imgur.com/5cwEE9o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
This concluded my project, as I successfully secured my Instances using IAM to control the level of access and permissions that users had to the EC2 instances. <br/>
<img src="https://i.imgur.com/2e2TM1X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
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
