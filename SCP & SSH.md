## Secure Copy Protocol (SCP)

### What is SCP?

The Secure Copy Protocol, or SCP, is a file transfer network protocol used to move files onto servers, and it fully supports encryption and authentication. SCP uses Secure Shell (SSH) mechanisms for data transfer and authentication to ensure the confidentiality of the data in transit.

### How Does SCP Work?

The SCP client can easily upload files to an SSH server or request files and directories for downloading. Then, the server sends all the subdirectories and the files that are available for download. The server controls the file downloads for security risks if the client is unintentionally connected to a malicious server. SCP is in fact a native command in most operating systems, such as macOS, Windows, or Linux.

### Advantages & Disadvantages of SCP

The major drawback to SCP is that it can only transfer files and is not as complete a process as other protocols.
Its major advantages are its robust security

### Status and Popularity

Although SCP can only transfer files, it can do it significantly faster than SFTP.
It is a handy command for users that spend a lot of time on the SSH protocol, like fast transferring speeds, and don't care about managing the remote server.

### Security

SCP can be called more of a combination of RCP and SSH than a protocol because the file transfer is performed using RCP and the SSH protocol, which provides authentication and encryption. SCP maintains the confidentiality of the data being transferred and protects the authenticity by blocking packet sniffers from extracting valuable information from the data packets.


### SCP & SSH by Windows 10 PowerShell CLI

- make sure OpenSSH client is installed in Windows.
  To verify, go to Start menu > Settings > Apps > optional features > scroll down and look for OpenSSH.
  This adds SSH functionality to Windows,
  and the user can use SSH from the Command Prompt (cmd.exe) or PowerShell.
- PowerShell is recommended over cmd.exe. PowerShell lets you use more Unix/Linux commands. Though Powershell may give a disconnect error.
- We recommend running both as Administrator.
- DO NOT use the ssh command at all in the same Terminal window.
  If you ssh into Tux, you won't be able to scp to/from your local computer (normally).

Example of how to use SCP : [Samples](https://support.cci.drexel.edu/cci-virtual-lab-resources/scp-or-ssh-or-sftp-gui-or-cli/scp-windows-10-powershell-cli-command-line-interface/)

pscp -scp Step_4_Deploy_Airflow_on_Docker.tar root@10.233.196.129:/home/milad/Desktop/Docker_Airflow

### Links
1. https://arc.cdata.com/resources/mft/scp.rst
2. 
