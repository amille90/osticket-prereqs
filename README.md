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

Step 1: Log into Azure and go to Virtual Machines
<p>
</p>
<img src="https://i.imgur.com/IUkxUna.png"/>
</p>
<p>

</p>
<br />
Step 2: Click on the +create tab and then press on Azure virtual machine.
</p>
<p>
<img src="https://i.imgur.com/xReHfgM.png"/>
</p>
<p>

</p>
<br />
Step 3: For resource group ceate a new one and call it OsTicketLab_RG or create your own name.
</p>
<p>
<img src="https://i.imgur.com/gKvWXMX.png"/>
</p>
<p>

</p>
<br />

Step 4: For virtual machine name call it osticket-vm, and choose appropiate region according to your location.
</p>
<p>
<img src="https://i.imgur.com/ClhJtv5.png"/>
</p>
<p>

</p>
<br />
Step 5: Choose an availabilty zone.
</p>
<p>
<img src="https://i.imgur.com/Tr3B098.png"/>
</p>
<p>

</p>
<br />
Step 6: For image choose Windows10 Pro, version 22H2.
</p>
<p>
<img src="https://i.imgur.com/yf3abbq.png"/>
</p>
<p>

</p>
<br />
Step 7: For size click on standard_D2s_v3-2 vcpus, 8 GiB memory.
</p>
<p>
<img src="https://i.imgur.com/KPYAXj7.png"/>
</p>
<p>

</p>
<br />
Step 8: Underneath Administrator Account create a username and password. These will be the credentials used to log onto the osTicket-vm within Remote Desktop. 
</p>
<p>
<img src="https://i.imgur.com/3g3S8Yh.png"/>
</p>
 
</p>
<br />
Step 9: Make sure to check off the checkbox underneath licensing.
</p>
<p>
<img src="https://i.imgur.com/x1RTUsx.png"/>
</p>
<p>

</p>
<br />
Step 10: Press Review and Create.
</p>
<p>
<img src="https://i.imgur.com/POciVcQ.png"/>
</p>
<p>

</p>
<br />
Step 11: Validation banner should pop up. Press Create.
</p>
<p>
<img src="https://i.imgur.com/5O25ETN.png"/>
</p>
<p>

</p>
<br />
Step 12: Next, deployment in progress page will pop up.
</p>
<p>
<img src="https://i.imgur.com/sG5ZzKS.png"/>
</p>
<p>

</p>
<br />
Step 13: Deployment should be complete.
</p>
<p>
<img src="https://i.imgur.com/gjW6bxW.png"/>
</p>
<p>

</p>
<br />
Step 14: Go back into virtual machines in Azure and you will now see the osTicket-vm added to your list of virtual machines created. Click on the osTicket-vm.
</p>
<p>
<img src="https://i.imgur.com/u3SRwrA.png"/>
</p>
<p>

</p>
<br />
Step 15: Copy the Public IP address of the  osTicket-vm.
</p>
<p>
<img src="https://i.imgur.com/GRFmURu.png"/>
</p>
<p>

</p>
<br />
Step 16: Go into remote desktop and add the osTicket-vm under add a pc. Make sure to paste the ip address within pc name box and in display name call it osTicket-vm then press save.
</p>
<p>
<img src="https://i.imgur.com/olfcXin.png"/>
</p>
<p>

</p>
<br />
Step 17: After adding the osTicket-vm pc now log into it with the credentials you created in the Adminstrator Account section while creating the virtual machine in Azure.
</p>
<p>
<img src="https://i.imgur.com/3NQh08n.png"/>
</p>
<p>

</p>
<br />


<h2>The next half of this project tutorial will now focus on installing the osTicket installation files.</h2>


</p>


</p>
<br />
Step 18: Upload the osTicket installation file onto your computer. 
</p>
<p>
<img src="https://i.imgur.com/0GYKC6z.png"/>
</p>
<p>

</p>
<br />
Step 19: Now download and drag the file onto your desktop. If you open up the file in file explorer you will see there are multiple files to be installed within that one zip folder. The following steps will walkthrough on how to do that.
</p>
<p>
<img src="https://i.imgur.com/hjaRlgZ.png"/> 
</p>
<img src="https://i.imgur.com/lSXJAFT.png"/>
<p>

</p>
<br />
Step 20: Go to the home menu of the osticket-vm remote desktop and type in Control Panel. Click on and open it. The control panel is where IIS and CGI will be installed and enabled.
</p>
<p>
<img src="https://i.imgur.com/YeDJ4Vy.png"/>
</p>
<p>

</p>
<br />
Step 21: Go to Programs/Uninstall a program.
</p>
<p>
<img src="https://i.imgur.com/s3POcNt.png"/>
</p>
<p>

</p>
<br />
Step 22: Next, click on Turn Windows features on or off.
</p>
<p>
<img src="https://i.imgur.com/zD4r7FM.png"/>
</p>
<p>

</p>
<br />
Step 23: The Turn Windows features on/off box will pop up. Check of Internet Information Services then expand the dropdown box.
</p>
<p>
<img src="https://i.imgur.com/O6aLeeE.png"/>
</p>
<p>

</p>
<br />
Step 24: Next expand World Wide Web services. 
</p>
<p>
<img src="https://i.imgur.com/Ct62fP1.png"/>
</p>
<p>
 
</p>
<br />
Step 25: Next expand Application Development features and check off CGI. 
</p>
<p>
<img src="https://i.imgur.com/08Kq3XK.png"/>
</p>
<p>

</p>
<br />
Step 26: Press OK.
</p>
<p>
<img src="https://i.imgur.com/bYbubpk.png"/>
</p>
<p>

</p>
<br />
Step 27: Windows will begin to search for and install the required files.
</p>
<p>
<img src="https://i.imgur.com/0f9vnC6.png"/>
</p>
<p>

</p>
<br />
Step 28: Press close after Windows has completed the requested changes.
</p>
<p>
<img src="https://i.imgur.com/Z5oNh7i.png"/>
</p>
<p>

</p>
<br />
Step 29: Next, go into the internet browser within the osTicket-vm remote desktop and type in 127.0.0.1. Press enter and the information services (IIS) page should pop up. FYI: If this page is not activated OsTicket can't be installed.
</p>
<p>
<img src="https://i.imgur.com/x3WJADU.png"/>
</p>
<p>

</p>
<br />
Step 30: From the osTicket installation files folder install the PHP Manager for IIS.(PHPManagerForIIS_V1.5.0.msi) Click on the file to open up.
</p>
<p>
<img src="https://i.imgur.com/11dNOgV.png"/>
</p>
<p>

</p>
<br />
Step 31: The first slide should pop up of the PHP Manager. Press next to continue. 
</p>
<p>
<img src="https://i.imgur.com/LfyWpwD.png"/>
</p>
<p>

</p>
<br />
Step 32: For the liscense agreement press agree and then click next.
</p>
<p>
<img src="https://i.imgur.com/Qiz42Yl.png"/>
</p>
<p>

</p>
<br />
Step 33: The PHP Manager will begin to install. Allow for it to finish installing. 
</p>
<p>
<img src="https://i.imgur.com/Epv6Eko.png"/>
</p>
<p>

</p>
<br />
Step 34: Installation is now complete. Press close. 
</p>
<p>
<img src="https://i.imgur.com/n0I0S9u.png"/>
</p>
<p>

</p>
<br />
Step 35: Next, install the rewrite module. Click on to open up. (rewrite_amd64_en-US.msi)
</p>
<p>
<img src="https://i.imgur.com/bgvF7bT.png"/>
</p>
<p>

</p>
<br />
Step 36: The first page of the rewrite module should pop up, press install.
</p>
<p>
<img src="https://i.imgur.com/MPEWNZX.png"/>
</p>
<p>

</p>
<br />
Step 37: The installation process will begin, let run until complete.
</p>
<p>
<img src="https://i.imgur.com/38ur5nD.png"/>
</p>
<p>

</p>
<br />
Step 38: Once the file is done being installed, press finish. 
</p>
<p>
<img src="https://i.imgur.com/FMwCAPF.png"/>
</p>
<p>

</p>
<br />
Step 39: Next, create a directory for the PHP folder.( C:\PHP) Click on and open up file explorer inside of osTicket-vm Remote Desktop.
</p>
<p>
<img src="https://i.imgur.com/MLNHyX0.png"/>
</p>
<p>

</p>
<br />
Step 40: Next, click on and open up C drive.
</p>
<p>
<img src="https://i.imgur.com/ZNFxCpL.png"/>
</p>
<p>

</p>
<br />
Step 41: Then right click to create new folder. 
</p>
<p>
<img src="https://i.imgur.com/7B2dYP0.png"/>
</p>
<p>

</p>
<br />
Step 42: Name the folder PHP.
</p>
<p>
<img src="https://i.imgur.com/yrqvzAT.png"/>
</p>
<p>

</p>
<br />
Step 43: Next, unzip and isntall the PHP 7.3.8 folder.(php-7.3.8-nts-Win32-VC15-x86.zip) Right click and press extract all.
</p>
<p>
<img src="https://i.imgur.com/TuYtgZe.png"/>
</p>
<p>

</p>
<br />
Step 44: The Select Destination and Extract Files page will pop up. 
</p>
<p>
<img src="https://i.imgur.com/CSugTVx.png"/>
</p>
<p>

</p>
<br />
Step 45: Press Browse.
</p>
<p>
<img src="https://i.imgur.com/Exw2dNc.png"/>
</p>
<p>

</p>
<br />
Step 46: Click on PHP folder and press select folder.
</p>
<p>
<img src="https://i.imgur.com/rimw5pE.png"/>
</p>
<p>

</p>
<br />
Step 47: The  destination and extract files page should come back up. Press Extract.
</p>
<p>
<img src="https://i.imgur.com/2aiP26w.png"/>
</p>
<p>

</p>
<br />
Step 48: Files will begin to download and install.
</p>
<p>
<img src="https://i.imgur.com/Q8Ucb7D.png"/>
</p>
<p>

</p>
<br />
Step 49: Next install the VC_redist.x86.exe file. Click on and open up.
</p>
<p>
<img src="https://i.imgur.com/wMV7x3r.png"/>
</p>
<p>

</p>
<br />
Step 50: The Microsoft Visual C++ page should pop up. Press Install. 
</p>
<p>
<img src="https://i.imgur.com/WDDereN.png"/>
</p>
<p>

</p>
<br />
Step 51: Installation setup should be successful. Press close.
</p>
<p>
<img src="https://i.imgur.com/zJRcfvo.png"/>
</p>
<p>

</p>
<br />
Step 52: Next, install the MySQL 5.5.62 file. (mysql-5.5.62-win32) Click on and open up.
</p>
<p>
<img src="https://i.imgur.com/RfgzvK5.png"/>
</p>
<p>

</p>
<br />
Step 53: The MySQL server page should pop up. Press next.
</p>
<p>
<img src="https://i.imgur.com/2HsOkeG.png"/>
</p>
<p>

</p>
<br />
Step 54: Make sure the accept terms box is checked off then press next for the end-user agreement.
</p>
<p>
<img src="https://i.imgur.com/kmNx9UQ.png"/>
</p>
<p>

</p>
<br />
Step 55: For setup type press 'Typical', then press next.
</p>
<p>
<img src="https://i.imgur.com/Tv7Nc1T.png"/>
</p>
<p>

</p>
<br />
Step 56: Click install.
</p>
<p>
<img src="https://i.imgur.com/MFYUsQY.png"/>
</p>
<p>

</p>
<br />
Step 57: Installation process should begin. Allow to finish installing then press next.
</p>
<p>
<img src="https://i.imgur.com/WXfYpCv.png"/>
</p>
<p>

</p>
<br />
Step 58: The MySQL completion page should come up, press finish.
</p>
<p>
<img src="https://i.imgur.com/VFykrpv.png"/>
</p>
<p>

<br />
Step 59: Next the MySQL Server Instance Configuration Wizard needs to be configured and installed. Press next. 
</p>
<p>
<img src="https://i.imgur.com/9QUTc4L.png"/>
</p>
<p>

</p>
<br />
Step 60: On the next page click on standard configuration and press next.
</p>
<p>
<img src="https://i.imgur.com/t9EXzn3.png"/>
</p>
<p>

</p>
<br />
Step 61: Press next.
</p>
<p>
<img src="https://i.imgur.com/47swqkz.png"/>
</p>
<p>

</p>
<br />
Step 62: Enter in the word "root" in both boxes, then press next.
</p>
<p>
<img src="https://i.imgur.com/QpnFLyr.png"/>
</p>
<p>

<br />
Step 63: Click on execute.
</p>
<p>
<img src="https://i.imgur.com/IKvATx9.png"/>
</p>
<p>

</p>
Step 64: Once all bullets have been checked off click on finish.
</p>
<p>
<img src="https://i.imgur.com/uD85vB0.png"/>
</p>
<p>

</p>
<br />
Step 65: Now right click on Internet Information Services in search menu of osTicket-vm remote desktop. Click on run as administrator and IIS should open up.
</p>
<p>
<img src="https://i.imgur.com/tlNrgZP.png"/>
</p>
<p>

</p>
<br />
Step 66: Click on PHP Manager.
</p>
<p>
<img src="https://i.imgur.com/PTgV1SO.png"/>
</p>
<p>

</p>
<br />
Step 67: Next press on Register new PHP version.
</p>
<p>
<img src="https://i.imgur.com/jKMWGmM.png"/>
</p>
<p>

</p>
<br />
Step 68: Then press the three dotted browse box on the right hand side. 
</p>
<p>
<img src="https://i.imgur.com/AegH9lr.png"/>
</p>
<p>

</p>
<br />
Step 69: Click on the PHP folder and click open.
</p>
<p>
<img src="https://i.imgur.com/9PB4s7b.png"/>
</p>
<p>

</p>
<br />
Step 70: Next click on the bottom link that says php-cgi.
</p>
<p>
<img src="https://i.imgur.com/S5LKXCn.png"/>
</p>
<p>

</p>
<br />
Step 71: Press open.
</p>
<p>
<img src="https://i.imgur.com/z1PRffD.png"/>
</p>
<p>

</p>
<br />
Step 72: The file link should upload in the path box. Press okay.
</p>
<p>
<img src="https://i.imgur.com/u2Su8Wm.png"/>
</p>
<p>

</p>
<br />
Step 73: Go into the IIS Manager, double/right click on the osticket-vm folder at the top left hand side and press the stop button.
</p>
<p>
<img src="https://i.imgur.com/RNXDl1o.png"/>
</p>
<p>

</p>
<br />
Step 74: Next press the start button to restart the server.
</p>
<p>
<img src="https://i.imgur.com/rxk9V0d.png"/>
</p>
<p>

</p>
<br />
Step 75: Go back into the osTicket file folder in file explorer and click on th osTicket-v1.15.8 zip file. Right click on it and press extract all.
</p>
<p>
<img src="https://i.imgur.com/3ehNcw4.png"/>
</p>
<p>

</p>
<br />
Step 76: Press the Extract button.
</p>
<p>
<img src="https://i.imgur.com/ZodW3Ct.png"/>
</p>
<p>

</p>
<br />
Step 77: Files should begin to download and install. Allow for the green bar to fill up to 100% completion. 
</p>
<p>
<img src="https://i.imgur.com/tmknFkW.png"/>
</p>
<p>

</p>
<br />
Step 78: Next go to and click on the Windows C drive in file explorer.
</p>
<p>
<img src="https://i.imgur.com/Z4u3UMW.png"/>
</p>
<p>

</p>
<br />
Step 79: Click on the inetpub folder.
</p>
<p>
<img src="https://i.imgur.com/5F4ao0t.png"/>
</p>
<p>

</p>
<br />
Step 80: From there click on the wwwroot folder.
</p>
<p>
<img src="https://i.imgur.com/lXa8ALO.png"/>
</p>
<p>

</p>
<br />
Step 81: Inside the wwwroot folder will be the two iisstart folders. Drag the "upload" folder from the osTicket-v1.15.8 file to the folder with both iisstarts. 
</p>
<p>
<img src="https://i.imgur.com/sgD6Ynm.png"/>
</p>
<p>

</p>
<br />
Step 82: The uplaod folder should now be inside the inetpub>wwwroot folder with the two iisstart.
</p>
<p>
<img src="https://i.imgur.com/R4mz4SC.png"/>
</p>
<p>

<br />
Step 83: Rename the folder to osTicket.
</p>
<p>
<img src="https://i.imgur.com/clIi2Ae.png"/>
</p>
<p>

</p>
<br />
Step 84: Now go back into IIS Manager, right click on osTicket in the upper left hand side and click stop.
</p>
<p>
<img src="https://i.imgur.com/vENeJAp.png"/>
</p>
<p>

</p>
<br />
Step 85: Next go back and press the start button to restart the server.
</p>
<p>
<img src="https://i.imgur.com/kxIRfDI.png"/>
</p>
<p>

</p>
<br />
Step 86: Click on View sites under Manager Server on the right hand side of the IIS app.
</p>
<p>
<img src="https://i.imgur.com/Idd3qiv.png"/>
</p>
<p>

</p>
<br />
Step 87: Expand down the sites folder, then expand down the default web site folder, then osTicket. Click on osTicket.
</p>
<p>
<img src="https://i.imgur.com/GefMdVs.png"/>
</p>
<p>

</p>
<br />
Step 88: On the right hand side of IIS Manager click on Browse*80(http).
</p>
<p>
<img src="https://i.imgur.com/FfsSx4C.png"/>
</p>
<p>

</p>
<br />
Step 89: Go back to the internet browser of the osTicket-vm remote desktop and the osTicket installer page should take place of the blue IIS hompage (127.0.0.1). To complete the osTicket installation some extentions need to be enabled.
</p>
<p>
<img src="https://i.imgur.com/b8sMW2D.png"/>
</p>
<p>

</p>
<br />
Step 90: Go back to IIS Manager and expand the Sites folder.
</p>
<p>
<img src="https://i.imgur.com/kNE330T.png"/>
</p>
<p>

</p>
<br />
Step 91: Next expand the Default Web Site folder and then expand the osTicket folder.
</p>
<p>
<img src="https://i.imgur.com/5Oyvaas.png"/>
</p>
<p>

</p>
<br />
Step 92: Double-click on PHP Manager.
</p>
<p>
<img src="https://i.imgur.com/5lFD3VA.png"/>
</p>
<p>

</p>
<br />
Step 93: Click on Enable or disable an extension link.
</p>
<p>
<img src="https://i.imgur.com/0KW7Fsv.png"/>
</p>
<p>

</p>
<br />
Step 94: Right click on php_imap.dll and press enable. 
</p>
<p>
<img src="https://i.imgur.com/qkNig6J.png"/>
</p>
<p>

</p>
<br />
Step 95: Right-click on php_intl.dll and press enable. 
</p>
<p>
<img src="https://i.imgur.com/MpG23DV.png"/>
</p>
<p>

</p>
<br />
Step 96: Right-click on php_opcache.dll and press enable. 
</p>
<p>
<img src="https://i.imgur.com/C2konm3.png"/>
</p>
<p>

</p>
<br />
Step 97: Next, go back into inetpub>wwwroot>osticket file/folder and rename the sampleconfig.php folder to just (ost-config.php).
</p>
<p>
<img src="https://i.imgur.com/Gn2UbEu.png"/>
</p>
<p>

</p>
<br />
Step 98: Right click on ost-config-php to assign permissions. Go to Properties. 
</p>
<p>
<img src="https://i.imgur.com/FRpBSbZ.png"/>
</p>
<p>

</p>
<br />
Step 99: Under the genreal tab make sure "include' is in the upper box then press ok.
</p>
<p>
<img src="https://i.imgur.com/PQRva00.png"/>
</p>
<p>

</p>
<br />
Step 100: Go to Security and then press Advanced. Click on Disbale inheritance.
</p>
<p>
<img src="https://i.imgur.com/GRiGSCu.png"/>
</p>
<p>

</p>
<br />
Step 101: Then click on remove all inherited permissions link.
</p>
<p>
<img src="https://i.imgur.com/GMTgDco.png"/>
</p>
<p>

</p>
<br />
Step 102: Press the add button.
</p>
<p>
<img src="https://i.imgur.com/ll8ZKNG.png"/>
</p>
<p>

</p>
<br />
Step 103: Click on select a principle.
</p>
<p>
<img src="https://i.imgur.com/4mnIRBo.png"/>
</p>
<p>

</p>
<br />
Step 104: Then type in everyone in the object name box.
</p>
<p>
<img src="https://i.imgur.com/u833tp9.png"/>
</p>
<p>

</p>
<br />
Step 105: Click on Check names.
</p>
<p>
<img src="https://i.imgur.com/7v5jWoS.png"/>
</p>
<p>

</p>
<br />
Step 106: Press Ok.
</p>
<p>
<img src="https://i.imgur.com/3tKVtQP.png"/>
</p>
<p>

</p>
<br />
Step 107: Check off the full control box and press ok.
</p>
<p>
<img src="https://i.imgur.com/6qYJkyy.png"/>
</p>
<p>

</p>
<br />
Step 108: Extentions and permissions should be enabled at this point of the installation and the osTicket Basic Installation page should be showing in your browser. Now its time to set up the system settings. Insert a helpdesk name, put in a default email and select primary language.
</p>
<p>
<img src="https://i.imgur.com/GWGeIDb.png"/>
</p>
<p>

</p>
<br />
Step 109: For admin user put in your first name, last name, an email address ( must be different from the one above), a username and password.
</p>
<p>
<img src="https://i.imgur.com/sEc5JrX.png"/>
</p>
<p>

</p>
<br />
Step 110: Before setting up database settings, HeidiSQL needs to be set up. Go back into the OsTicket file folder on the desktop of the osTicket-vm remote desktop. Click on HeidiSQL_ 12.3.0.6589 and the license agreement page should pop up.
</p>
<p>
<img src="https://i.imgur.com/atV6PW3.png"/>
</p>
<p>

</p>
<br />
Step 111: Press on the I accept agreement option and then click next.
</p>
<p>
<img src="https://i.imgur.com/8JkuVaN.png"/>
</p>
<p>

</p>
<br />
Step 112: Click next on the Selct Destination Location page. 
</p>
<p>
<img src="https://i.imgur.com/AMV7dnh.png"/>
</p>
<p>

</p>
<br />
Step 113: Press next on Select Start Menu Folder. 
</p>
<p>
<img src="https://i.imgur.com/pUIuVwQ.png"/>
</p>
<p>

</p>
<br />
Step 114: Click install on the Ready to Install page. 
</p>
<p>
<img src="https://i.imgur.com/IQPChH5.png"/>
</p>
<p>

</p>
<br />
Step 115: File should begin to install, make sure it install's until completion. 
</p>
<p>
<img src="https://i.imgur.com/YbiMXlK.png"/>
</p>
<p>

</p>
<br />
Step 116: On the Donate page just press finish. 
</p>
<p>
<img src="https://i.imgur.com/TSwTDGT.png"/>
</p>
<p>

</p>
<br />
Step 117: Next a new session needs to be created in HeidiSQL. Click on new. 
</p>
<p>
<img src="https://i.imgur.com/pomtLQL.png"/>
</p>
<p>

</p>
<br />
Step 118: Type in the word root in both the username and password boxes on the right hand side of the session manager app. 
</p>
<p>
<img src="https://i.imgur.com/ypKp9kK.png"/>
</p>
<p>

</p>
<br />
Step 119: Click open then connect to session.
</p>
<p>
<img src="https://i.imgur.com/fSzstEn.png"/>
</p>
<p>

</p>
<br />
Step 120: Right click on dolphin image in upper left hand corner to create a new database.
</p>
<p>
<img src="https://i.imgur.com/x2JIZEL.png"/>
</p>
<p>

</p>
<br />
Step 121: Click on create new, then database
</p>
<p>
<img src="https://i.imgur.com/t46f1T1.png"/>
</p>
<p>

</p>
<br />
Step 122: Create database box should pop up. Insert osTicket in the name box, then press ok.
</p>
<p>
<img src="https://i.imgur.com/DuRWDsV.png"/>
</p>
<p>

</p>
<br />
Step 123: Go back to OsTicket in the web browser of the remote desktop. Under Database settings for MySQL Databse box type in osTicket and for the MYSQL username and password type in the word "root". Click install now.
</p>
<p>
<img src="https://i.imgur.com/uydglTg.png"/>
</p>
<p>

</p>
<br />
Step 124: OsTicket is finally installed. Make sure to bookmark the osTicket url link and the Your Staff Control Panel Link for the next project tutorial walkthrough.
</p>
<p>
<img src="https://i.imgur.com/E79sRQ5.png"/>
</p>.
<p>

</p>
<br />
Step 125: Here is the support center page where backend users will use to submit their tickets.
</p>
<p>
<img src="https://i.imgur.com/HPZ9sG0.png"/>
</p>
<p>

</p>
<br />
Step 126: Here is the page where desk agents and admins login to process and resolve the tickets.
</p>
This here concludes the project tutorial of the prerequisites, installation and walkthrough of osTicket Ticketing System.
</p>
<p>
<img src="https://i.imgur.com/Dqe0dhN.png"/>
</p>
<p>























