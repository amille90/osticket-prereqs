<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This project tutorial outlines, observes, and walks through the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)/ CGI

<h2>Operating Systems Used </h2>

- Windows10 Pro</b> (21H2)

<h2>List of Prerequisites</h2>

- Computer Desktop/Laptop
- Wifi Connection
- Azure Account
- OsTicket Installation zip files
- Internet Information Services IIS/CGI

<h2>Installation Steps</h2>

<h2>The first half of this tutorial will focus on setting up the osTicket Virtual Machine in Azure. </h2>

</p>

Step 1:
<p>
<img src="https://i.imgur.com/IUkxUna.png"/>
</p>
<p>
Log into Azure and go to Virtual Machines
</p>
<br />
Step 2:
<p>
<img src="https://i.imgur.com/xReHfgM.png"/>
</p>
<p>
Click on the +create tab and then press on Azure virtual machine.
</p>
<br />
Step 3:
<p>
<img src="https://i.imgur.com/gKvWXMX.png"/>
</p>
<p>
For resource group ceate a new one and call it OsTicketLab_RG or create your own name.
</p>
<br />

Step 4:
<p>
<img src="https://i.imgur.com/ClhJtv5.png"/>
</p>
<p>
For virtual machine name call it osticket-vm, and choose appropiate region according to your location.
</p>
<br />
Step 5: 
<p>
<img src="https://i.imgur.com/Tr3B098.png"/>
</p>
<p>
Choose an availabilty zone.
</p>
<br />
Step 6:
<p>
<img src="https://i.imgur.com/yf3abbq.png"/>
</p>
<p>
For image choose Windows10 Pro, version 22H2.
</p>
<br />
Step 7:
<p>
<img src="https://i.imgur.com/KPYAXj7.png"/>
</p>
<p>
For size click on standard_D2s_v3-2 vcpus, 8 GiB memory.
</p>
<br />
Step 8:
<p>
<img src="https://i.imgur.com/3g3S8Yh.png"/>
</p>
Underneath Administrator Account create a username and password. These will be the credentials used to log onto the osTicket-vm within Remote Desktop. 
</p>
<br />
Step 9:
<p>
<img src="https://i.imgur.com/x1RTUsx.png"/>
</p>
<p>
Make sure to check off the checkbox underneath licensing.
</p>
<br />
Step 10:
<p>
<img src="https://i.imgur.com/POciVcQ.png"/>
</p>
<p>
Press Review and Create.
</p>
<br />
Step 11:
<p>
<img src="https://i.imgur.com/5O25ETN.png"/>
</p>
<p>
Validation banner should pop up. Press Create.
</p>
<br />
Step 12:
<p>
<img src="https://i.imgur.com/sG5ZzKS.png"/>
</p>
<p>
Next, deployment in progress page will pop up.
</p>
<br />
Step 13:
<p>
<img src="https://i.imgur.com/gjW6bxW.png"/>
</p>
<p>
Deployment should be complete.
</p>
<br />
Step 14:
<p>
<img src="https://i.imgur.com/u3SRwrA.png"/>
</p>
<p>
Go back into virtual machines in Azure and you will now see the osTicket-vm added to your list of virtual machines created. Click on the osTicket-vm.
</p>
<br />
Step 15:
<p>
<img src="https://i.imgur.com/GRFmURu.png"/>
</p>
<p>
Copy the Public IP address of the  osTicket-vm.
</p>
<br />
Step 16:
<p>
<img src="https://i.imgur.com/olfcXin.png"/>
</p>
<p>
Go into remote desktop and add the osTicket-vm under add a pc. Make sure to paste the ip adddress within pc name box and in display name call it osTicket-vm then press save.
</p>
<br />
Step 17:
<p>
<img src="https://i.imgur.com/3NQh08n.png"/>
</p>
<p>
After adding the osTicket-vm pc now log into it with the credentials you created in the Adminstrator Account section while creating the virtual machine in Azure.
</p>
<br />


<h2>The next half of this project tutorial will now focus on installing the osTicket installation files.</h2>


</p>


</p>
<br />
Step 18:
<p>

<img src="https://i.imgur.com/0GYKC6z.png"/>
</p>
<p>
Upload the osTicket installation file onto your computer. 
</p>
<br />
Step 19:
<p>
<img src="https://i.imgur.com/hjaRlgZ.png"/> 
</p>
<img src="https://i.imgur.com/lSXJAFT.png"/>
<p>
Now download and drag the file onto your desktop. If you open up the file in file explorer you will see there are multiple files to be installed within that one zip folder. The following steps will walkthrough on how to do that.
</p>
<br />
Step 20: 
<p>
<img src="https://i.imgur.com/YeDJ4Vy.png"/>
</p>
<p>
Go to the home menu of the osticket-vm remote desktop and type in Control Panel. Click on and open it. The control panel is where IIS and CGI will be installed and enabled.
</p>
<br />
Step 21:
<p>
<img src="https://i.imgur.com/s3POcNt.png"/>
</p>
<p>
Go to Programs/Uninstall a program.
</p>
<br />
Step 22:
<p>
<img src="https://i.imgur.com/zD4r7FM.png"/>
</p>
<p>
Next, click on Turn Windows features on or off.
</p>
<br />
Step 23:
<p>
<img src="https://i.imgur.com/O6aLeeE.png"/>
</p>
<p>
The Turn Windows features on/off box will pop up. Check of Internet Information Services then expand the dropdown box.
</p>
<br />
Step 24:
<p>
<img src="https://i.imgur.com/Ct62fP1.png"/>
</p>
<p>
Next expand World Wide Web services. 
</p>
<br />
Step 25:
<p>
<img src="https://i.imgur.com/08Kq3XK.png"/>
</p>
<p>
Next expand Application Development features and check off CGI. 
</p>
<br />
Step 26:
<p>
<img src="https://i.imgur.com/bYbubpk.png"/>
</p>
<p>
Press OK.
</p>
<br />
Step 27:
<p>
<img src="https://i.imgur.com/0f9vnC6.png"/>
</p>
<p>
Windows will begin to search for and install the required files.
</p>
<br />
Step 28: 
<p>
<img src="https://i.imgur.com/Z5oNh7i.png"/>
</p>
<p>
Press close after Windows has completed the requested changes.
</p>
<br />
Step 29:
<p>
<img src="https://i.imgur.com/x3WJADU.png"/>
</p>
<p>
Next, go into the internet browser within the osTicket-vm remote desktop and type in 127.0.0.1. Press enter and the information services (IIS) page should pop up. FYI: If this page is not activated OsTicket can't be installed.
</p>
<br />
Step 28:
<p>
<img src="https://i.imgur.com/11dNOgV.png"/>
</p>
<p>
From the osTicket installation files folder install the PHP Manager for IIS.(PHPManagerForIIS_V1.5.0.msi) Click on the file to open up.
</p>
<br />
Step 29:
<p>
<img src="https://i.imgur.com/LfyWpwD.png"/>
</p>
<p>
The first slide should pop up of the PHP Manager. Press next to continue. 
</p>
<br />
Step 30:
<p>
<img src="https://i.imgur.com/Qiz42Yl.png"/>
</p>
<p>
For the liscense agreement press agree and them click next.
</p>
<br />
Step 31:
<p>
<img src="https://i.imgur.com/Epv6Eko.png"/>
</p>
<p>
The PHP Manager will begin to install. Alllow for it to finish downloading. 
</p>
<br />
Step 32:
<p>
<img src="https://i.imgur.com/n0I0S9u.png"/>
</p>
<p>
Installation is now complete. Press close. 
</p>
<br />
Step 33:
<p>
<img src="https://i.imgur.com/bgvF7bT.png"/>
</p>
<p>
Next, install the rewrite module. Click on to open up. (rewrite_amd64_en-US.msi) 
</p>
<br />
Step 34:
<p>
<img src="https://i.imgur.com/MPEWNZX.png"/>
</p>
<p>
The first page of the rewrite module should pop up, press install.
</p>
<br />
Step 35:
<p>
<img src="https://i.imgur.com/38ur5nD.png"/>
</p>
<p>
The installation process will begin, let run until complete.
</p>
<br />
Step 36:
<p>
<img src="https://i.imgur.com/FMwCAPF.png"/>
</p>
<p>
Once the file is done being installed, press finish. 
</p>
<br />
Step 37:
<p>
<img src="https://i.imgur.com/MLNHyX0.png"/>
</p>
<p>
Next, create a directory for the PHP folder.( C:\PHP) Click on and open up file explorer inside of osTicket-vm Remote Desktop.
</p>
<br />
Step 38:
<p>
<img src="https://i.imgur.com/ZNFxCpL.png"/>
</p>
<p>
Next, click on and open up C drive.
</p>
<br />
39:
<p>
<img src="https://i.imgur.com/7B2dYP0.png"/>
</p>
<p>
Then right click to create new folder. 
</p>
<br />
Step 40:
<p>
<img src="https://i.imgur.com/yrqvzAT.png"/>
</p>
<p>
Name the folder PHP.
</p>
<br />
Step 41:
<p>
<img src="https://i.imgur.com/TuYtgZe.png"/>
</p>
<p>
Next, unzip and isntall the PHP 7.3.8 folder.(php-7.3.8-nts-Win32-VC15-x86.zip) Right click and press extract all.
</p>
<br />
Step 42:
<p>
<img src="https://i.imgur.com/CSugTVx.png"/>
</p>
<p>
The Select Destination and Extract Files page will pop up. 
</p>
<br />
Step 43:
<p>
<img src="https://i.imgur.com/Exw2dNc.png"/>
</p>
<p>
Press Browse.
</p>
<br />
Step 44:
<p>
<img src="https://i.imgur.com/rimw5pE.png"/>
</p>
<p>
Click on PHP folder and press select folder.
</p>
<br />
45:
<p>
<img src="https://i.imgur.com/2aiP26w.png"/>
</p>
<p>
The  destination and extract files page should come back up. Press Extract.
</p>
<br />
Step 46:
<p>
<img src="https://i.imgur.com/Q8Ucb7D.png"/>
</p>
<p>
Files will begin to download and install.
</p>
<br />
Step 47:
<p>
<img src="https://i.imgur.com/wMV7x3r.png"/>
</p>
<p>
Next install the VC_redist.x86.exe file. Click on and open up.
</p>
<br />
Step 48:
<p>
<img src="https://i.imgur.com/WDDereN.png"/>
</p>
<p>
The Microsoft Visual C++ page should pop up. Press Install. 
</p>
<br />
Step 49:
<p>
<img src="https://i.imgur.com/zJRcfvo.png"/>
</p>
<p>
Installation setup should be successful. Press close.
</p>
<br />
Step 50:
<p>
<img src="https://i.imgur.com/RfgzvK5.png"/>
</p>
<p>
Next, install the MySQL 5.5.62 file. (mysql-5.5.62-win32) Click on and open up.
</p>
<br />
Step 51:
<p>
<img src="https://i.imgur.com/2HsOkeG.png"/>
</p>
<p>
The MySQL serve page should pop up. Press next.
</p>
<br />
Step 52:
<p>
<img src="https://i.imgur.com/kmNx9UQ.png"/>
</p>
<p>
Press next for the end-user agreement.
</p>
<br />
Step 53:
<p>
<img src="https://i.imgur.com/Tv7Nc1T.png"/>
</p>
<p>
For setup type press 'Typical', then press next.
</p>
<br />
Step 54:
<p>
<img src="https://i.imgur.com/MFYUsQY.png"/>
</p>
<p>
Click install.
</p>
<br />
Step 55:
<p>
<img src="https://i.imgur.com/WXfYpCv.png"/>
</p>
<p>
Installation process should begin. Allow to finish installing then press next.
</p>
<br />
Step 56:
<p>
<img src="https://i.imgur.com/VFykrpv.png"/>
</p>
<p>
The MySQL completion page should come up, press finish.
<br />
Step 57:
<p>
<img src="https://i.imgur.com/9QUTc4L.png"/>
</p>
<p>
Next the MySQL Server Instance Configuration Wizard needs to be configured and installed. Press next. 
</p>
<br />
Step 58:
<p>
<img src="https://i.imgur.com/t9EXzn3.png"/>
</p>
<p>
On the next page click on standard configuration and press next.
</p>
<br />
Step 59:
<p>
<img src="https://i.imgur.com/47swqkz.png"/>
</p>
<p>
Press next.
</p>
<br />
Step 60:
<p>
<img src="https://i.imgur.com/QpnFLyr.png"/>
</p>
<p>
Enter in the word "root" in both boxes.
<br />
Step 61:
<p>
<img src="https://i.imgur.com/IKvATx9.png"/>
</p>
<p>
Click on execute.
</p>
<br />
Step 62:
<p>
<img src="https://i.imgur.com/uD85vB0.png"/>
</p>
<p>
Once all bullets have been checked off click on finish.
</p>
<br />
Step 63:
<p>
<img src="https://i.imgur.com/tlNrgZP.png"/>
</p>
<p>
Now right click on Internet Information Services in search menu of osTicket-vm remote desktop. Click on run as administrator and IIS should open up.
</p>
<br />
Step 64:
<p>
<img src="https://i.imgur.com/PTgV1SO.png"/>
</p>
<p>
Click on PHP Manager.
</p>
<br />
Step 65:
<p>
<img src="https://i.imgur.com/jKMWGmM.png"/>
</p>
<p>
Next press on Register new PHP version.
</p>
<br />
Step 66:
<p>
<img src="https://i.imgur.com/AegH9lr.png"/>
</p>
<p>
Then press the three dotted browse box on the right hand side. 
</p>
<br />
Step 67:
<p>
<img src="https://i.imgur.com/9PB4s7b.png"/>
</p>
<p>
Click on the PHP folder and click open.
</p>
<br />
Step 68:
<p>
<img src="https://i.imgur.com/S5LKXCn.png"/>
</p>
<p>
Next click on the bottom link that says php-cgi.
</p>
<br />
Step 69:
<p>
<img src="https://i.imgur.com/z1PRffD.png"/>
</p>
<p>
Press open.
</p>
<br />
Step 70:
<p>
<img src="https://i.imgur.com/u2Su8Wm.png"/>
</p>
<p>
The file link should upload in the path box. Press okay.
</p>
<br />
Step 71:
<p>
<img src="https://i.imgur.com/RNXDl1o.png"/>
</p>
<p>
Go into the IIS Manager, double/right click on the osticket-vm folder at the top left hand side and press the stop button.
</p>
<br />
Step 72:
<p>
<img src="https://i.imgur.com/rxk9V0d.png"/>
</p>
<p>
Next press the start button to restart the server. 
</p>
<br />
73:
<p>
<img src="https://i.imgur.com/3ehNcw4.png"/>
</p>
<p>
Go back into the osTicket file folder in file explorer and click on th osTicket-v1.15.8 zip file. Right click on it and press extract all.
</p>
<br />
74:
<p>
<img src="https://i.imgur.com/ZodW3Ct.png"/>
</p>
<p>
Press the Extract button on the next page.
</p>
<br />
75:
<p>
<img src="https://i.imgur.com/tmknFkW.png"/>
</p>
<p>
Files should begin to download and install. Allow for the green bar to fill up to 100% completion. 
</p>
<br />
76:
<p>
<img src="https://i.imgur.com/Z4u3UMW.png"/>
</p>
<p>
Next go to and click on the Windows C drive in file explorer.
</p>
<br />
77:
<p>
<img src="https://i.imgur.com/5F4ao0t.png"/>
</p>
<p>
Click on the inetpub folder.
</p>
<br />
78:
<p>
<img src="https://i.imgur.com/lXa8ALO.png"/>
</p>
<p>
From there click on the wwwroot folder.
</p>
<br />
Step 79:
<p>
<img src="https://i.imgur.com/sgD6Ynm.png"/>
</p>
<p>
Inside the wwwroot folder will be the two iisstart folders. Drag the "upload" folder from the osTicket-v1.15.8 file to the folder with both iisstarts. 
</p>
<br />
Step 80:
<p>
<img src="https://i.imgur.com/R4mz4SC.png"/>
</p>
<p>
The uplaod folder should now be inside the inetpub>wwwroot folder with the two iisstart.
<br />
Step 81:
<p>
<img src="https://i.imgur.com/clIi2Ae.png"/>
</p>
<p>
Rename the folder to osTicket.
</p>
<br />
Step 82:
<p>
<img src="https://i.imgur.com/vENeJAp.png"/>
</p>
<p>
Now go back into IIS Manager, right click on osTicket in the upper left hand side and click stop.
</p>
<br />
Step 83:
<p>
<img src="https://i.imgur.com/kxIRfDI.png"/>
</p>
<p>
Next go back and press the start button to restart the server.
</p>
<br />
Step 84:
<p>
<img src="https://i.imgur.com/Idd3qiv.png"/>
</p>
<p>
Click on View sites under Manager Server on the right hand side of the IIS app.
</p>
<br />
Step 85:
<p>
<img src="https://i.imgur.com/GefMdVs.png"/>
</p>
<p>
Expand down the sites folder, then expand down the default web site folder, then osTicket. Click on osTicket.
</p>
<br />
Step 86:
<p>
<img src="https://i.imgur.com/FfsSx4C.png"/>
</p>
<p>
On the right hand side of IIS Manager click on Browse*80(http).
</p>
<br />
Step 87:
<p>
<img src="https://i.imgur.com/b8sMW2D.png"/>
</p>
<p>
Go back to the internet browser of the osTicket-vm remote desktop and the osTicket installer page should take place of the blue IIS hompage (127.0.0.1). To complete the osTicket installation some extentions need to be enabled.
</p>
<br />
Step 88:
<p>
<img src="https://i.imgur.com/kNE330T.png"/>
</p>
<p>
Go back to IIS Manager and expand the Sites folder.
</p>
<br />
Step 89:
<p>
<img src="https://i.imgur.com/5Oyvaas.png"/>
</p>
<p>
Next expand the Default Web Site folder and then expand the osTicket folder.
</p>
<br />
Step 90:
<p>
<img src="https://i.imgur.com/5lFD3VA.png"/>
</p>
<p>
Double-click on PHP Manager.
</p>
<br />
Step 91:
<p>
<img src="https://i.imgur.com/0KW7Fsv.png"/>
</p>
<p>
Click on Enable or disable an extension link.
</p>
<br />
Step 92:
<p>
<img src="https://i.imgur.com/qkNig6J.png"/>
</p>
<p>
Right click on php_imap.dll and press enable. 
</p>
<br />
Step 93:
<p>
<img src="https://i.imgur.com/MpG23DV.png"/>
</p>
<p>
Right-click on php_intl.dll and press enable. 
</p>
<br />
Step 94:
<p>
<img src="https://i.imgur.com/C2konm3.png"/>
</p>
<p>
Right-click on php_opcache.dll and press enable. 
</p>
<br />
Step 95:
<p>
<img src="https://i.imgur.com/Gn2UbEu.png"/>
</p>
<p>
Next, go back into inetpub>wwwroot>osticket file/folder and rename the sampleconfig.php folder to just (ost-config.php).
</p>
<br />
Step 96:
<p>
<img src="https://i.imgur.com/FRpBSbZ.png"/>
</p>
<p>
Right click on ost-config-php to assign permissions. Go to Properties. 
</p>
<br />
Step 97:
<p>
<img src="https://i.imgur.com/PQRva00.png"/>
</p>
<p>
Under the genreal tab make sure "include' is in the upper box then press ok.
</p>
<br />
Step 98:
<p>
<img src="https://i.imgur.com/GRiGSCu.png"/>
</p>
<p>
Go to Security and then press Advanced. Click on Disbale inheritance.
</p>
<br />
Step 99:
<p>
<img src="https://i.imgur.com/GMTgDco.png"/>
</p>
<p>
Then click on remove all inherited permissions link.
</p>
<br />
Step 100:
<p>
<img src="https://i.imgur.com/ll8ZKNG.png"/>
</p>
<p>
Press the add button.
</p>
<br />
Step 102:
<p>
<img src="https://i.imgur.com/4mnIRBo.png"/>
</p>
<p>
Click on select a principle.
</p>
<br />
Step 103:
<p>
<img src="https://i.imgur.com/u833tp9.png"/>
</p>
<p>
Then type in everyone in th object name box.
</p>
<br />
Step 104:
<p>
<img src="https://i.imgur.com/7v5jWoS.png"/>
</p>
<p>
Click on Check names. .
</p>
<br />
Step 105:
<p>
<img src="https://i.imgur.com/3tKVtQP.png"/>
</p>
<p>
Press Ok.
</p>
<br />
Step 106:
<p>
<img src="https://i.imgur.com/6qYJkyy.png"/>
</p>
<p>
Check off the full control box and press ok.
</p>
<br />
Step 107:
<p>
<img src="https://i.imgur.com/GWGeIDb.png"/>
</p>
<p>
Extentions and permissions should be enabled at this point of the installation and the osTicket Basic Installation page should be showing in your browser. Now its time to set up the system settings. Insert a helpdesk name, put in a default email and select primary language.
</p>
<br />
Step 108:
<p>
<img src="https://i.imgur.com/sEc5JrX.png"/>
</p>
<p>
For admin user put in your first name, last name, an email address ( must be different from the one above), a username and password.
</p>
<br />
Step 109:
<p>
<img src="https://i.imgur.com/atV6PW3.png"/>
</p>
<p>
Before setting up database settings, HeidiSQL needs to be set up. Go back into the OsTicket file folder on the desktop of the osTicket-vm remote desktop. Click on HeidiSQL_ 12.3.0.6589 and the license agreement page should pop up.
</p>
<br />
Step 110:
<p>
<img src="https://i.imgur.com/8JkuVaN.png"/>
</p>
<p>
Press on the I accept agreement option and then click next.
</p>
<br />
Step 111:
<p>
<img src="https://i.imgur.com/AMV7dnh.png"/>
</p>
<p>
Click next on the Selct Destination Location page. 
</p>
<br />
Step 112:
<p>
<img src="https://i.imgur.com/pUIuVwQ.png"/>
</p>
<p>
Press next on Select Start Menu Folder. 
</p>
<br />
Step 113:
<p>
<img src="https://i.imgur.com/IQPChH5.png"/>
</p>
<p>
Click install on the Ready to Install page. 
</p>
<br />
Step 114:
<p>
<img src="https://i.imgur.com/YbiMXlK.png"/>
</p>
<p>
File should begin to install, make sure it install's until completion. 
</p>
<br />
Step 113:
<p>
<img src="https://i.imgur.com/TSwTDGT.png"/>
</p>
<p>
On the Donate page just press finish. 
</p>
<br />
Step 114:
<p>
<img src="https://i.imgur.com/pomtLQL.png"/>
</p>
<p>
Next a new session needs to be created in HeidiSQL. Click on new. 
</p>
<br />
Step 115:
<p>
<img src="https://i.imgur.com/ypKp9kK.png"/>
</p>
<p>
Type in the word root in both the username and password boxes on the right hand side of the session manager app. 
</p>
<br />
116:
<p>
<img src="https://i.imgur.com/fSzstEn.png"/>
</p>
<p>
Click open then connect to session.
</p>
<br />
Step 117:
<p>
<img src="https://i.imgur.com/x2JIZEL.png"/>
</p>
<p>
Right click on dolphin image in upper left hand corner to create a new database.
</p>
<br />
Step 118:
<p>
<img src="https://i.imgur.com/t46f1T1.png"/>
</p>
<p>
Click on create new, then database
</p>
<br />
Step 119:
<p>
<img src="https://i.imgur.com/DuRWDsV.png"/>
</p>
<p>
Create database box should pop up. Insert osTicket in the name box, then press ok.
</p>
<br />
Step 120:
<p>
<img src="https://i.imgur.com/uydglTg.png"/>
</p>
<p>
Go back to OsTicket in the web browser of the remote desktop. Under Database settings for MySQL Databse box type in osTicket and for the MYSQL username and password type in the word "root". Click install now.
</p>
<br />
Step 121:
<p>
<img src="https://i.imgur.com/E79sRQ5.png"/>
</p>.
<p>
OsTicket is finally installed. Make sure to bookmark the osTicket url link and the Your Staff Control Panel Link for the next project tutorial walkthrough. 
</p>
<br />
Step 122:
<p>
<img src="https://i.imgur.com/HPZ9sG0.png"/>
</p>
<p>
Here is the support center page where backend users will use to submit thier tickets.
</p>
<br />
Step 123:
<p>
<img src="https://i.imgur.com/Dqe0dhN.png"/>
</p>
<p>
Here is the page where desk agents and admins login to process and resolve the tickets.

This here concludes the project tutorial of the prerequisites, installation and walkthrough of the osTicket Ticketing System.
</p>
<br />



https://i.imgur.com/DuRWDsV.png

https://i.imgur.com/x2JIZEL.png


















