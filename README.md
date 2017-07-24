# GDB_Visual_Studio_2017_Windows_Subsystem_Linux
How to debug in Windows Subsystem Linux (WSL) using GDB debugger

## Prerequisites
* Must be on Windows 10 and it is up to date.

* Must be on the latest Insider Preview build 1703 or higher (Creators Update) [Link](https://insider.windows.com/Install/PC)

* Must have WSL (Windows Subsystem Linux) installed. I used this great how to from How-To Geek to install Bash on Ubuntu on Windows. [Link](https://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/)

* Must have Visual Studio 2017 installed. You can use the the free edition (Visual Studio Community 2017). [Download here](https://www.visualstudio.com/downloads/)

## Setting up Visual Studio to Compile and Debug 

1. Install metapackage build-essential, gdb server, and openssh server
	1. Open WSL
	2. `sudo apt-get update`
	3. `sudo apt-get install -y build-essential`
	4. `sudo apt-get install -y gdbserver`
	5. `sudo apt=get install -y openssh-server`
2. Open sshd_config using vi, emacs, or nano. I prefer nano as it is much easier to use for beginners.
	1. `nano /etc/ssh/sshd_config`
	2. set PasswordAuhentication to yes
3. Generate SSH keys
	1. `sudo ssh-keygen -A`
4. Start openssh server
	1. `sudo service ssh start`
5. Create a console application in Visual Studio
6. Target x64
7. Add SSh connections
	1. Host Name: localhost
	2. Port: 22
	3. User Name: "Enter your bash user name"
	4. Password: "Enter password associated with your bash user name"
