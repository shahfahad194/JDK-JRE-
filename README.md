# JDK-JRE-Installation
9 Installation of the JDK and the JRE on Microsoft Windows Platforms
This topic includes the following sections:

System Requirements for Installing the JDK and the JRE on 64-Bit Windows Platform

JDK and JRE Installation Instruction Notation for Windows

JDK Installation Instructions for Windows

JRE Installation Instructions for Windows

Windows Registry Settings

Beginning to Use the JDK

Uninstalling the JDK on Windows

Uninstalling the JRE on Windows

JDK Installation Troubleshooting

Windows Online Installation and Java Update FAQ

System Requirements for Installing the JDK and the JRE on 64-Bit Windows Platform
The JDK and the JRE have minimum processor, disk space, and memory requirements for 64-bit Windows platform.

Before installing the JDK or the JRE on your 64-bit Windows platform, you must verify that it meets the following minimum processor, disk space, and memory requirements.

Processor Requirements

Both the JDK and JRE require at minimum a Pentium 2 266 MHz processor.

Disk Space Requirements

For JDK 10, you are given the option of installing the following features:

Development Tools

Source Code

Public Java Runtime Environment

When you install 64-bit JDK, then 64-bit public JRE also gets installed. The following table provides the disk requirements for the installed features:

JDK	Installed Image
Development Tools: 64-bit platform	500 MB
Source Code	54.2 MB
JRE	Installed Image
Public Java Runtime Environment	200 MB
Java Update	2 MB
Memory Requirements

On Windows 64-bit operating systems, the Java runtime requires a minimum of 128 MB of memory.

Note:

The minimum physical RAM is required to run graphically based applications. More RAM is recommended for applets running within a browser using the Java Plug-in. Running with less memory may cause disk swapping, which has a severe effect on performance. Very large programs may require more RAM for adequate performance.

Note:

For supported processors and browsers, see Oracle JDK Certified Systems Configurations.

JDK and JRE Installation Instruction Notation for Windows
For any text in this document that contains the following notation, you must substitute the appropriate update version number:

interim.update.patch

For example:

If you are downloading the JDK installer for 64-bit systems for update 10 Interim 0, Update 2, and Patch 1, then the file name jdk-10.interim.update.patch_windows-x64_bin.exe becomes jdk-10.0.2.1_windows-x64_bin.exe.

If you are downloading the JRE installer for 64-bit systems for update 10 Interim 0, Update 2, and Patch 1, then the file name jre-10.interim.update.patch_windows-x64_bin.exe becomes jre-10.0.2.1_windows-x64_bin.exe.

JDK Installation Instructions for Windows
You run a self-installing executable file to unpack and install the JDK on Windows computers.

Install JDK on Windows computers by performing the actions described in the following topics:

Downloading the JDK Installer

Running the JDK Installer

Installing the JDK Silently

Setting the PATH Environment Variable

Downloading the JDK Installer
In a browser, go to the Java SE Development Kit 10 Downloads page and click Accept License Agreement. Under the Download menu, click the Download link that corresponds to the .exe for your version of Windows.

Download the file jdk-10.interim.update.patch_windows-x64_bin.exe.

Note:

Verify the successful completion of file download by comparing the file size on the download page and your local drive.
Running the JDK Installer
You must have administrator privilage to install the JDK on Microsoft Windows.
To run the JDK installer:
Start the JDK 10 installer by double-clicking the installer's icon or file name in the download location.
Follow the instructions provided by the Installation wizard.
The JDK includes the JavaFX SDK, a private JRE, and the Java Mission Control tools suite. The installer integrates the JavaFX SDK into the JDK installation directory.
After the installation is complete, delete the downloaded file to recover the disk space.
Installing the JDK Silently
Instead of double-clicking or opening the JDK installer, you can perform a silent, noninteractive, JDK installation by using command-line arguments.

The following table lists example installation scenarios and the commands required to perform them. The notation jdk stands for the downloaded installer file base name, such as jdk-10_windows-x64_bin.exe.

Installation Scenario	Command
Install JDK and public JRE in silent mode.	
jdk.exe /s
Install development tools and source code in silent mode but not the public JRE.	
jdk.exe /s ADDLOCAL="ToolsFeature,SourceFeature"
Install development tools, source code, and the public JRE in silent mode.	
jdk.exe /s ADDLOCAL="ToolsFeature,SourceFeature,PublicjreFeature"
Install the public JRE in the specified directory C:\test in silent mode.	
jdk.exe /s /INSTALLDIRPUBJRE=C:\test
Setting the PATH Environment Variable
It is useful to set the PATH variable permanently for JDK 10 so that it is persistent after rebooting.

Note:

The PATH variable is set automatically for the JRE. This topic only applies to the JDK.

If you do not set the PATH variable, then you must specify the full path to the executable file every time that you run it. For example:

C:\> "C:\Program Files\Java\jdk-10\bin\javac" MyClass.java
To set the PATH variable permanently, add the full path of the jdk-10\bin directory to the PATH variable. Typically, the full path is:
C:\Program Files\Java\jdk-10\bin
To set the PATH variable on Microsoft Windows:
Select Control Panel and then System.
Click Advanced and then Environment Variables.
Add the location of the bin folder of the JDK installation to the PATH variable in System Variables.
Note:

The PATH environment variable is a series of directories separated by semicolons (;) and is not case-sensitive. Microsoft Windows looks for programs in the PATH directories in order, from left to right.

You should only have one bin directory for a JDK in the path at a time. Those following the first instance are ignored.

If you are not sure where to add the JDK path, append it.

The new path takes effect in each new command window that you open after setting the PATH variable.

The following is a typical value for the PATH variable:

C:\WINDOWS\system32;C:\WINDOWS;"C:\Program Files\Java\jdk-10\bin"
JRE Installation Instructions for Windows
When installing JRE on Windows computers, you must select the JRE installer that is appropriate for your Windows system.

The 64-bit Windows operating systems come with a 64-bit Internet Explorer (IE) browser as the standard (default) for viewing web pages.

Install JRE on Windows computers by performing the actions described in the following topics:

JRE Proxy Settings and Authentication

Downloading the JRE Installer

Running the JRE Installer

JRE Proxy Settings and Authentication
To use the Windows Online Installer, you must be connected to the internet.

If you are running behind a proxy server, then you must have your proxy settings correctly configured. If they are not configured, or are incorrectly configured, then the installer will terminate with the following message:

The installer cannot proceed with the current Internet Connection settings.

Please visit the following website for more information.

https://www.java.com/en/download/help/

If you see this message, check your proxy settings:

In the Control Panel , double-click Internet Options, select the Connections tab, and click the LAN Settings.

If you do not know what the correct settings should be, check with your internet provider or system administrator.

Downloading the JRE Installer
The JRE Installer is located on the Java SE Runtime Environment 10 Downloads page.

In a browser, go to the Java SE Runtime Environment 10 Downloads page.
The following JRE installers are available for you to download:

Windows Offline: jre-10.interim.update.patch_windows-x64_bin.exe

Windows Tar: jre-10.interim.update.patch_windows-x64_bin.tar.gz

Download the JRE installer according to your requirement.
Note:

The Windows Offline installer and Windows installer contains everything that is required to install the JRE.

The Microsoft Windows Installer (MSI) Enterprise JRE Installer is also available, which enables you to install the JRE across your enterprise. It requires a commercial license for use in production.

Click Accept License Agreement, and then, under the Download menu, click the link that corresponds to the installer for your version of Windows.
Note the file size specified on the download page and, after the download has completed, verify that you have downloaded the complete file.
Running the JRE Installer
You must have Administrative privileges in order to install the JRE on Microsoft Windows.
To run the JRE installer:
Start the JRE 10 Installer by double-clicking the installer's icon or file name in the download location.
Follow the instructions provided by the Installation wizard.
The installer notifies you if Java content is disabled in web browsers and provides instructions for enabling it. If you previously chose to hide some of the security prompts for applets and Java Web Start applications, then the installer provides an option for restoring the prompts.
After the installation is complete, delete the downloaded file to recover disk space.
Note:

The private JRE installed with the JDK is not registered. To register the JRE, you must set the PATH environment variable to point to JAVA_HOME\bin, where JAVA_HOME is the location where you installed the private JRE . See Setting the PATH Environment Variable.

By default, the Java Access Bridge is disabled. To enable it, see Enabling and Testing Java Access Bridge in the Java Platform, Standard Edition Java Accessibility Guide.

To access essential Java information and functions in Microsoft Windows 7 and Windows 10 machines, after installation, click the Start menu and then select Java. The Java directory provides access to Help, Check for Updates, and Configure Java.

The Microsoft Windows 8 and Windows 8.1 do not have a Start menu. However, the Java information is available in the following Start directory: %ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs.

Windows Registry Settings
The installation program for the Microsoft Windows version of the Java SE Runtime Environment uses the registry to store path and version information.

It creates the following registry keys:

HKEY_LOCAL_MACHINE\Software\JavaSoft\JRE

This key contains the string CurrentVersion, with a value that is the highest installed version on the system.

HKEY_LOCAL_MACHINE\Software\JavaSoft\JRE\<version>

This key contains the following string values:
JavaHome: the full path name of the directory in which the JRE is installed

RuntimeLib: the full path name of the Java runtime DLL

HKEY_LOCAL_MACHINE\Software\JavaSoft\Java Web Start\

This key is created for Java Web Start.

If there are two versions of JDK or JRE installed on a system, one with the new version-string format introduced in JDK 10, and the other with the older version format, then there will be two different CurrentVersion registry key values. For example, if JDK 1.8.0 and JDK 10 are installed, then the following registry keys are created:

"HKEY_LOCAL_MACHINE\SOFTWARE\JavaSoft\Java Development Kit" for JDK 1.8.0 and "HKEY_LOCAL_MACHINE\SOFTWARE\JavaSoft\JDK" for JDK 10.

The registry layout for this example is:

"HKEY_LOCAL_MACHINE\SOFTWARE\JavaSoft\JDK\10"
"HKEY_LOCAL_MACHINE\SOFTWARE\JavaSoft\JDK"
        "@CurrentVersion" = 10
"HKEY_LOCAL_MACHINE\SOFTWARE\JavaSoft\Java Development Kit\1.8"
"HKEY_LOCAL_MACHINE\SOFTWARE\JavaSoft\Java Development Kit\1.8.0"
"HKEY_LOCAL_MACHINE\SOFTWARE\JavaSoft\Java Development Kit"
        "@CurrentVersion" = 1.8
The @CurrentVersion is a registry string in the "JDK" or "Java Development Kit" key.

For the same example, if the JRE is installed, then the registry layout is:

"HKEY_LOCAL_MACHINE\SOFTWARE\JavaSoft\JRE\10"
"HKEY_LOCAL_MACHINE\SOFTWARE\JavaSoft\JRE"
        "@CurrentVersion" = 10
"HKEY_LOCAL_MACHINE\SOFTWARE\JavaSoft\Java Runtime Environment\1.8"
"HKEY_LOCAL_MACHINE\SOFTWARE\JavaSoft\Java Runtime Environment\1.8.0"
"HKEY_LOCAL_MACHINE\SOFTWARE\JavaSoft\Java Runtime Environment"
        "@CurrentVersion" = 1.8
The @CurrentVersion is a registry string in the "JRE" or "Java Runtime Environment" key.

Beginning to Use the JDK
Use the Java item in the Windows Start menu to access essential Java information and functions, including Help, API documentation, the Java Control Panel, checking for updates, and Java Mission Control.

Java Start Menu Installed by JDK
During JDK install, Java menu items are added to the Windows Start menu to provide easy access to Java resources and a Java Development Kit folder is created in the Windows Start menu, which contains the following items:

Reference Documentation: Opens the Online API documentation web page.

Java Mission Control: Opens the Java Mission Control profiling and diagnostics tools suite.

Note:

Java Mission Control is a commercial feature available to users with a Java SE Advanced license.

During JDK installation and uninstallation processes, the appropriate start menu items are updated so that they are associated with the latest JDK version on the system

Note:

The Windows 7 and Windows 10 have a Start menu; however, the menu is not available in Windows 8 and Windows 8.1. The JDK and Java information in Windows 8 and Windows 8.1 is available in the following Start directory: %ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs.
Java Start Menu Installed by JRE
During JRE installation, Java menu items are added to the Windows Start menu to provide easy access to Java resources and a Java folder is created in the Windows Start menu, which contains the following items:

About Java: Opens the Java Control Panel with focus on the General tab. The tab displays the latest JRE version installed on the system.

Check for Updates: Opens the Java Control Panel with focus on the Update tab

Configure Java: Opens the Java Control Panel with focus on the General tab

Get Help: Opens the Java Help Center

Visit Java.com: Opens the Java Download page

During JRE installation and uninstallation processes, the appropriate start menu items are updated so that they are associated with the latest JRE version on the system.

Note:

The Windows 7 and Windows 10 have Start menu, however the menu is not available in Windows 8 and Windows 8.1. The JRE and Java information in Windows 8 and Windows 8.1 is available in the following Start directory: %ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs.
Java Web Start
Java Web Start is an application-deployment technology that gives you the power to run full-featured applications with a single click from your web browser.

With Java Web Start, you can download and run applications, such as a complete spreadsheet program or an internet chat client, without going through complicated installation procedures. With Java Web Start, you run applications simply by clicking a web page link. If the application is not present on your computer, Java Web Start automatically downloads all necessary files. It then caches the files on your computer so that the application is always ready to be run anytime that you want - either from an icon on your desktop or from the browser link. No matter which method you use to run the application, the most current, available version of the application is always presented to you.

Upgrading from Previous Versions

If you have a previous version of Java Web Start, do not uninstall it. Uninstalling it will cause the download cache to be cleared, and all previously installed Java Web Start application data will have to be downloaded again. The new version will write over previous installations and automatically update browsers to use the new version. The configuration files and the program files folder used by Java Web Start have changed, but all your settings will remain intact after the upgrade because Java Web Start will translate your settings to the new form.

Uninstallation

The only way to uninstall Java Web Start is to uninstall the JDK or JRE. Uninstalling the JDK or JRE will not, however, remove the cache for previous versions of Java Web Start. Previous releases have separate uninstallation instructions for Java Web Start.

You may see a misleading message if you do the following:

Download and cache a Java Web Start application with the JDK or JRE.

Remove the JDK or JRE using Add or Remove Programs from the Windows Control Panel.

Remove the Java Web Start application using Add or Remove Programs.

When you remove the application, you see an Uninstaller Error dialog box saying:

An error occurred while trying to remove Java-Application:nameApp. It may have already been uninstalled. Would you like to remove Java-Application: name App from the Add or Remove program list?

If you say Yes to this, then you will see another Uninstaller Error dialog box saying:

You do not have sufficient access to remove Java-Application:nameApp from the Add or Remove Program list. Please contact your system administrator.

The message is displayed when you have removed the Java Web Start application while uninstallating the JDK or JRE, but this is not reflected in the Add or Remove Programs. Refresh the Add or Remove Programs by pressing F5 or reopen the panel.

To avoid seeing the misleading message, either press F5 or reopen the dialog box. Any Java Web Start application that was downloaded and cached with the JDK or JRE will no longer appear in the list of currently installed programs.

Java Plug-in
Java Plug-in technology, included as part of the JRE, establishes a connection between popular browsers and the Java platform. This connection enables applets on websites to be run within a browser on the desktop.

The Java Plug-in is automatically enabled for supported web browsers during installation of the JRE. No user intervention is necessary.

Note:

In Java SE 10, the version of the Java Plug-in that is available in versions of the JRE prior to Java SE 6 Update 10 has been deprecated. However, this earlier version of the Java Plug-in is still shipped with Java SE 10 for compatibility purposes but is no longer fully supported. It will be removed in a future release.

Option to Disable the JRE Out-of-Date Warning
When the installed JRE falls below the security baseline or passes its built-in expiration date, an additional warning is shown to users to update their installed JRE to the latest version. For businesses that manage the update process centrally, users attempting to update their JRE individually, may cause problems.

A deployment property, deployment.expiration.check.enabled is available that can be used to disable the JRE out of date warning. To suppress this specific warning message, add the following entry in the deployment properties file:

deployment.expiration.check.enabled=false

To disable automatic updates, on the Update tab of the Java Control Panel, deselect the Check for Updates Automatically check box.

Uninstalling the JDK on Windows
To uninstall JDK 10, use the Add/Remove Programs utility in the Microsoft Windows Control Panel.
Uninstalling the JRE on Windows
Use either of the following ways to uninstall JRE:

Go to Add/Remove Programs utility in the Microsoft Windows Control Panel and uninstall the older versions of JRE.

Remove JRE using the online Java Uninstall Tool.

The Java Removal Tool is integrated with the JRE installer. After JRE 10 is installed, the Java Removal Tool provides the list of outdated Java versions in the system and helps you to remove them.

Note:

The Java Uninstall tool will not run if your system administrator specified a deployment rule set in your organization.

A deployment rule set enables enterprises to manage their Java desktop environment directly and continue using legacy business applications in an environment of ever-tightening Java applet and Java Web Start application security policies. A deployment rule set enables administrators to specify rules for applets and Java Web Start applications; these rules may specify that a specific JRE version must be used. Consequently, the Java Uninstall tool will not run if it detects a deployment rule set to ensure that no required JREs are uninstalled.

See Deployment Rule Set in the Java Platform, Standard Edition Deployment Guide.

JDK Installation Troubleshooting
The following sections provide tips for working around problems that are sometimes seen during or while following installation instructions.

System Error During Decompression

If you see the error message system error during decompression, then you might not have enough space on the disk that contains your TEMP directory.

Program Cannot Be Run in DOS Mode

If you see the error message This program cannot be run in DOS mode, then do the following:

Open the MS-DOS shell or command prompt window.

Right-click the title bar.

Select Properties.

Select the Program tab.

Click Advanced.

Ensure that the item Prevent MS-DOS-based programs from detecting Windows is not selected.

Select OK.

Select OK again.

Exit the MS-DOS shell.

Restart your computer.

Source Files in Notepad

In Microsoft Windows, when you create a new file in Microsoft Notepad and then save it for the first time, Notepad usually adds the .txt extension to the file name. Therefore, a file that you name Test.java is actually saved as Test.java.txt. Note that you cannot see the .txt extension unless you turn on the viewing of file extensions (in Microsoft Windows Explorer, deselect Hide file extensions for known file types under Folder Options). To prevent the .txt extension, enclose the file name in quotation marks, such as "Test.java" when entering information in the Save As dialog box.

Characters That Are Not Part of the System Code Page

It is possible to name directories using characters that are not part of the system locale's code page. If such a directory is part of the installation path, then generic error 1722 occurs, and installation is not completed. Error 1722 is a Windows installer error code. It indicates that the installation process has failed. The exact reason for this error is not known at this time.

To prevent this problem, ensure that the user and system locales are identical, and that the installation path contains only characters that are part of the system locale's code page. User and system locales can be set in the Regional Options or Regional Settings control panel.

The associated bug number is 4895647.

Windows Online Installation and Java Update FAQ
These are frequently asked questions about JDK 10 and JRE 10 online installation and Java updates on Windows computers.

1. I downloaded the installer and it is less than 1 megabyte. Why is it so small?

The Windows Online Installer for the JRE will download more installer files. Using this installer helps users to avoid downloading unnecessary files.

2. I had the Java Control Panel open for Java Update and the About tab showed the version of the JRE installed in my computer. Then I ran Java Update, and the version of the JRE that the Java Control Panel is showing has not changed. Why is this?

You need to close and restart the Java Control Panel to get the updated Control Panel.

3. Netscape/Mozilla is not working correctly with Java Plug-in. Why?

First, close all the browsers sessions. If this does not work, reboot the system and try again.

4. I try to install on the D:\ drive and Java Update is still installing files onto the C:\ drive. Why?

Regardless of whether an alternate target directory was selected, Java Update needs to install some files on the Windows system drive.

5. How can I uninstall the Java Update version that I just installed?

If you want to uninstall the JRE, then use the Add/Remove Programs utility in the Microsoft Windows . Select the Control Panel and then Add/Remove Programs.

6. After the JRE bootstrap installer is downloaded and executed, why does the message "This installer cannot proceed with the current Internet Connection settings of your system. In your Windows Control Panel, please check Internet Options -> Connections to make sure the settings and proxy information are correct." appear?

The JRE bootstrap installer uses the system Internet Connection settings to connect to the web for downloading extra files. If you are behind a firewall and require proxy settings, then ensure that the proxy settings in Internet Options/Internet Properties are set up properly (select Start, then Control Panel, then Internet Options/Internet Properties, then Connections, and then LAN Settings). If you can browse the external web (for example, outside the firewall) with Internet Explorer, then your proxy settings are properly set up. The installer does not understand the proxy settings specified in Netscape/Mozilla.

7. I found the jusched.exe process running in the background of my system after installing JRE. Is there a way to shut it down?

The jusched.exe is the scheduler process of Java Update. This process runs automatically. To shut in the Java Control Panel on the Update tab, deselect the Check for Updates Automatically check box.

8. When I click the Update Now button from the Java Control Panel, it complains about the system being "offline." What does that mean?

Java Update can be run only if the system is connected to the network. A system that is not connected to the network is referred to as being offline. When the Update Now is clicked, it will check the online/offline status of your system. If your computer does not have internet access, then the error message is displayed. Check that your system is currently connected to the internet and try again.

9. I followed the instructions to install a specific version of the JRE. After the installation, a message is displayed from system tray saying an update is available for download. What should I do?

The message is part of the Java Auto Update mechanism, which detects at user login time if a newer version of the JRE is available for download. In the system tray, click the Java Update icon to download and install the update.

10. I encountered the error "This installation package could not be opened. Contact the application vendor to verify that this is a valid Windows Installer package." when running the Java SE installer.

There are several possible reasons for this error to be displayed; a few are listed:

Network connection fails.

Download manager software interrupts the download process.

Another application, such as an antivirus application, may interrupt the installation process.

To address these problems, ensure that the third-party downloader applications are turned off and the network connection is configured properly. Also, if a proxy is in use, then ensure that the proxy authentication is turned off.

11. I encountered the error "Error 1722. There is a problem with this Windows installer package. A program run as part of the setup did not finish as expected. Contact your support personnel or package vendor."

See Error 1722: Problem with Windows Installer Package. If you encounter any other errors or issues, then you can access Java Help Center, which contains solutions for issues that you might encounter when downloading and installing Java on your system. In particular, you can search for solutions by error number. Searching for "Error 1722" returns a solution to this issue.
