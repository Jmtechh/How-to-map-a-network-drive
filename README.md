<h1>How to map a network drive</h1>


<h2>Description</h2>
The goal of this lab is to map a network drive by granting specific domain users exclusive access to a drive by assigning them to a designated security group with the necessary permissions.


<h2>Utilities Used</h2>

- <b>Virtualbox</b>
- <b>virtual machines</b>
- <b>Active directory</b>

<h2>Environments Used </h2>

- <b>Windows 10 OS</b>
- <b>Windows 10 server OS</b> 

<h2>Program walk-through:</h2>

The first step I took was opening VirtualBox and navigating to the File and Sharing section in Server Manager on the Domain Controller VM to create two shared drives, HR and Personal, for domain users.

<img src="https://i.imgur.com/XCPDTmE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>   

The HR and Personal drive.

<img src="https://i.imgur.com/Y3ghgB0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

After creating the shared drives, I set up a security group for the **HR drive**. This allows me to control access by adding users to the group—only those who are members will be granted permission to the drive.

<img src="https://i.imgur.com/mhMmQnp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

I then created a security group for the Personal drive.

<img src="https://i.imgur.com/9IYaK29.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

The two security groups for both drives.

<img src="https://i.imgur.com/NKnSfFU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Next, I added a user named Lucy, who is part of the **HR team/folder** in **Active Directory**. Since she belongs to HR, I assigned her to the **HR security group**, which will grant her access to the **HR folder** once the drive configurations are complete.

<img src="https://i.imgur.com/yoLkxgH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

I then added three additional users, this time assigning them to the **Personal security group**.

<img src="https://i.imgur.com/jhYBPHo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Next, I accessed the **Personal drive settings** and, under the **Security** section, added the **Personal security group** I had created earlier. This ensures that the three users assigned to this group can now access the **Personal drive** through their individual accounts.

<img src="https://i.imgur.com/rrx7zUg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

After configuring the **Personal drive settings**, I shared the drive and enabled **read/write permissions**, allowing users in the **Personal security group** to add and edit files on the **Personal drive** from their individual accounts.

<img src="https://i.imgur.com/SsHzzQA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

I then configured the **HR drive settings** in the same way, but this time, I added the **HR security group**. This ensures that **Lucy**, as a member of the group, will have access to the **HR drive**.

<img src="https://i.imgur.com/4U1VGiF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

After configuring the **HR drive settings**, I shared the drive and enabled **read/write permissions**, allowing members of the **HR security group** to add and edit files on the **HR drive** from their individual accounts.

<img src="https://i.imgur.com/nGfm9rK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

I then logged into Lucy's account but on a different VM.

<img src="https://i.imgur.com/wvLgGVX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

In the image below, the **Domain Controller** is on the left, and the **Client VM**, where Lucy is signed in, is on the right. I mapped the **HR drive** from the **Domain Controller**, ensuring that Lucy can access it each time she logs into her account.

<img src="https://i.imgur.com/XgB4MzR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

The HR drive has been created and is now visible in the file explorer.

<img src="https://i.imgur.com/XvqM6WN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Next, I used **Active Directory** to automatically create a **Personal drive** for **Adam**. This method allows me to map the drive without needing to log into his account manually.

<img src="https://i.imgur.com/K8uGVGN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Once I sign in, I should see a drive labeled **Personal** in their **File Explorer**.

<img src="https://i.imgur.com/XdHb4B6.png" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/c8vUJOE.png" width="80%" alt="Disk Sanitization Steps"/>







