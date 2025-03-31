<h1>How to map a network drive</h1>


<h2>Description</h2>
The goal of this lab is to grant specific domain users exclusive access to a drive by assigning them to a designated security group with the necessary permissions.


<h2>Utilities Used</h2>

- <b>Virtualbox</b>
- <b>virtual machines</b>
- <b>Active directory</b>

<h2>Environments Used </h2>

- <b>Windows 10 OS</b>
- <b>Windows 10 server OS</b> 

<h2>Program walk-through:</h2>

The first thing I did was I opened up virtual box and went to the server manger (ON THE DOMAIN CONTROLLER VM) file and sharing area in order to create the two drives(HR and Personal) which are to be shared with other users on the domain.

<img src="https://i.imgur.com/XCPDTmE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>   

The HR and Personal drive.

<img src="https://i.imgur.com/Y3ghgB0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

After creating the share drives. I then created a security group for the HR drive. This allows me to add users to this specific security group which enables users access to the drive based on weather or not they are apart of the security group.

<img src="https://i.imgur.com/mhMmQnp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

I then created a secuirty group for the Personal drive.

<img src="https://i.imgur.com/9IYaK29.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

The two security groups for both drives.

<img src="https://i.imgur.com/NKnSfFU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

I then added a user named Lucy. Lucy is apart of the HR team/folder in active directory which is why I've added her to this specific security group. Lucy being added to the HR secuirty group will give her access to the HR folder when I finish the configurations on the HR drive.

<img src="https://i.imgur.com/yoLkxgH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

I then add three different users but this time I add them to the Personal secuirty group.

<img src="https://i.imgur.com/jhYBPHo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

I then went to the Personal drives settings and on the securty section I specifically added the personal secuirity group which I created earlier. This will enable the three users that I added to the personal secuirty group to now have access to the personal drive on there own specific accounts.

<img src="https://i.imgur.com/rrx7zUg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

After configuring the Personal drive settings I then shared the drive and enable it to read/write so that the users who are apart of the Personal security group can add and edit the Personal drive on their personal account.

<img src="https://i.imgur.com/SsHzzQA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

I then went to the HR drives settings and did the same thing but instead I added the HR secuirty group to the HR drive. This will enable Lucy to have access to this drive since she is a member of the HR secuirty group.

<img src="https://i.imgur.com/4U1VGiF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

After configuring the HR drive settings I then shared the drive and enable it to read/write so that the users who are apart of the Personal security group can add and edit the Personal drive on their personal account.

<img src="https://i.imgur.com/nGfm9rK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

I then logged into Lucy's account but on a different VM.

<img src="https://i.imgur.com/wvLgGVX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

In the image below I have the domain controller on the left and the client VM where Lucy is signed in on the right. I'm now making the drive which I created on the domain controller accessible to Lucy by

<img src="https://i.imgur.com/XgB4MzR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/XvqM6WN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/K8uGVGN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/XdHb4B6.png" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/c8vUJOE.png" width="80%" alt="Disk Sanitization Steps"/>







