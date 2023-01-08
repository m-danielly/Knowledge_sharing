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

#### Example 1
scp yourTuxUserid@tux.cs.drexel.edu:test.txt "C: \Users\Win10userID\OneDrive - Drexel University\Desktop"\
or...
scp mjg88@tux.cs.drexel.edu:test.txt "C: \Users\mjg88\OneDrive - Drexel University\Desktop"\

Copying the test.txt file from your remote Tux home folder to your local Windows PC computer's desktop folder.
Quotes needed around the Desktop folder path on your computer because of the spaces in the OneDrive folder name.
Also, need a backslash or \ after the quoted file path to indicate it's a folder.

#### Example 2
scp yourTuxUserid@tux.cs.drexel.edu:test.txt .
or...
scp mjg88@tux.cs.drexel.edu:test.txt .

Copying a file named test.txt from your remote Tux home folder to your local Windows PC computer.
The period at the end indicates that the file will be copied to the current directory or folder you are in within cmd.exe or PowerShell.

More example of how to use SCP : [Samples](https://support.cci.drexel.edu/cci-virtual-lab-resources/scp-or-ssh-or-sftp-gui-or-cli/scp-windows-10-powershell-cli-command-line-interface/)


### PSCP

PSCP, the PuTTY Secure Copy client, is a tool for transferring files securely between computers using an SSH connection.
If you have an SSH-2 server, you might prefer PSFTP (see chapter 6) for interactive use. PSFTP does not in general work with SSH-1 servers


### PSCP Usage

Once you've got a console window to type into, you can just type pscp on its own to bring up a usage message. This tells you the version of PSCP you're using, and gives you a brief summary of how to use PSCP:

Z:\owendadmin>pscp
PuTTY Secure Copy client
Release 0.60
Usage: pscp [options] [user@]host:source target
       pscp [options] source [source...] [user@]host:target
       pscp [options] -ls [user@]host:filespec
Options:
  - V        print version information and exit
  - pgpfp    print PGP key fingerprints and exit
  - p        preserve file attributes
  - q        quiet, don't show statistics
  - r        copy directories recursively
  - v        show verbose messages
  - load sessname  Load settings from saved session
  - P port   connect to specified port
  - l user   connect with specified username
  - pw passw login with specified password
  - 1 -2     force use of particular SSH protocol version
  - 4 -6     force use of IPv4 or IPv6
  - C        enable compression
  - i key    private key file for authentication
  - noagent  disable use of Pageant
  - agent    enable use of Pageant
  - batch    disable all interactive prompts
  - unsafe   allow server-side wildcards (DANGEROUS)
  - sftp     force use of SFTP protocol
  - scp      force use of SCP protocol
 
(PSCP's interface is much like the Unix scp command, if you're familiar with that.) 

shell
```
pscp -scp Step_4_Deploy_Airflow_on_Docker.tar root@10.233.196.129:/home/milad/Desktop/Docker_Airflow
```
### Links
1. [what is SCP](https://arc.cdata.com/resources/mft/scp.rst
2. [PSCP](https://the.earth.li/~sgtatham/putty/0.60/htmldoc/Chapter5.html)
3. [install SSH](https://github.com/PowerShell/Win32-OpenSSH)
4. [install Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
5. [](https://phoenixnap.com/kb/linux-scp-command)
