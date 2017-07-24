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
