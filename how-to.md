# This will become a how-to to set up your Minecraft server at home and references to other articles to make it accessible to your friends.

## What's my setup?  
I have a little home server with Proxmox installed, and in that, I'll create a virtual machine with Debian as the OS that will run the Minecraft server.  
I have a few different approaches to share the server with the internet. I'll explain how to set up my router and a DynDNS service that only works with a public IP, and the other ones rely on a server on the internet that works as a reverse tunnel server.

Please note: I'm doing this for fun, to step out of my comfort zone and improve my writing skills. I plan on doing this one bit at a time and might skip parts if the muse isn't passing my way. So please be patient.  
If you have any constructive feedback or questions, just get in touch.  

## The Java installation for the Debian server

At the time of this writing, Debian's apt packages provide a version of Java that's required to run Minecraft 1.21. So let's start by downloading OpenJDK 21 as a .deb package from [Oracle's official website](https://www.oracle.com/de/java/technologies/downloads/#java21). I'll pick the x64 Debian package for my system, copy the link, and download it using wget. After that, I'll start the installation process with apt.

```bash
wget https://download.oracle.com/java/21/latest/jdk-21_linux-x64_bin.deb
sudo apt install ./jdk-21_linux-x64_bin.deb -y
