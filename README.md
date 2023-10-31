# Linux-on-Windows
<img src="images/ubuntu_start.gif">

Linux on Windows dream setup with VMware. My goal was to have the benefits of Linux distributions like their command line with Windows. It should also include a shared folder so you can share files seamlessly between Windows and Linux. In this guide I will walk you through how you can build your own one-click portal to the world of Linux and close it as easily as you open it.

## Prerequisites
(These versions of the software were used at the time of writing this guide.)
- Windows (Windows 10 19045.3636)
- VMware Workstaion (17.5.0 build-22583795)
- Linux ISO (ubuntu-22.04.3-desktop-amd64.iso)

## Setting up the VMware Virtual Machine
*Hint: You can also use VMware Player after you installed VMware Workstation. We only need some componets of VMware Workstation.*
Once you have clicked on "File->New Virtual Machine..." (Make sure you have updated your RAM and CPU cores to the appropriate levels for your system. For example 25% of your PC's RAM and 75% of your PC's CPU cores. Also give your VM about 50GB of disk space if you can. This space will only be used if needed, so no worries) and boot your Linux image. Next you are going to install your VMware Tools this can sometimes happen automatically, just resize your VMware window and check if the Linux window resizes too, if it does you are good to go.

## Connect to the Virtual Machine via SSH
Right-click on your newly created VM and press "Settings..." and add a second Network Adapter. Check Host-only as Network connection.
<img src="images/Network.png">
We need this adapter to have a static IP address for our SSH connection.