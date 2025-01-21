---
layout: page
title: Resources
description: Resources for the course.
---

# Development Environment

## Simulator Setup
[Link to Simulator Setup](https://liberating-dash-9ac.notion.site/F1Tenth-Simulator-Setup-5a013b6a723b490cbf6881a42a94d63f)

## Virtual Machine options

- Use one of options for Hypervisors given below or setup natively
- VMs are provided for VirtualBox and Parallels
- Credentials:
    - Username : `cse4568`
    - Password : `cse4568` (for VirtualBox)
    - Password : `cse4568#` (for Parallels)
- Note : Multipass is an alternative to using VirtualBox and Parallels (which is paid) and requires more work so limited support will be available from instructors

### VirtualBox [Recommended] for x86

This is a free and open-source virtualization software that can be used to run virtual machines.

- [Oracle VM VirtualBox](https://www.virtualbox.org/)
    
- After downloading VirtualBox, install it on your machine.
- Once installed, open VirtualBox and click on the "Import" button to import a virtual machine.
- Select the pre-configured virtual machine file, this should have the extension ".ova" or ".ovf"
- Follow the prompts to import the virtual machine.
- Once imported, select the virtual machine and click on "Start" button to launch it.
- [[Pre-configured Virtual Machine download link]](https://buffalo.box.com/s/qedq5ph8otgbaf2cay4fzd2x01btju8e)

### Parallels Desktop [Recommended] for Apple Silicon (M1x,M2x)

This is a paid virtualization software that can be used to run virtual machines.

- [Run Windows on Mac - Parallels Desktop 18 Virtual Machine for Mac](https://www.parallels.com/products/desktop/)
    
- After downloading Parallels Desktop, install it on your machine.
- Once installed, open Parallels Desktop and click on the "File" menu, select "Import".
- Select the pre-configured virtual machine file, this should have the extension ".pvm" or ".hdd"
- Follow the prompts to import the virtual machine.
- Once imported, select the virtual machine and click on "Start" button to launch it.
- [[Pre-configured Virtual Machine download link]](https://ubuffalo-my.sharepoint.com/:u:/g/personal/yashturk_buffalo_edu/EY-SkGPh42xEktLh65jzUhgBGQMxxa8Zf22FB2TuUA571g?e=DUDUxz)

<aside>
💡 ROS Noetic is already installed on the VMs. If you plan on using a native installation, please follow the instructions given below on Ubuntu 20.04 (Focal).

</aside>

### Multipass [Unsupported]

Multipass is a simple and lightweight tool for creating and managing virtual machines on Linux, Windows, and macOS. It uses the hypervisor built into your operating system to create and manage VMs, making it an easy and efficient option for running Ubuntu and ROS on your local machine.

To use Multipass for your assignments:

- To install Multipass, please visit the following link: [https://multipass.run/](https://multipass.run/)
- Once installed, you can create an Ubuntu 20.04 VM with the command: `multipass launch --name ubuntu2004 -c 2 -d 20G -m 4G`
- To access the VM, you can use the command `multipass shell ubuntu2004`
- To install a desktop environment and `xrdp` for GUI access, you can use the following commands:
    
    ```bash
    sudo apt update
    sudo apt install -y xfce4 xfce4-goodies xorg dbus-x11 x11-xserver-utils
    sudo apt install -y xrdp
    sudo apt install -y ubuntu-desktop
    ```
    
- To install Microsoft Remote Desktop. Its available on your respective app stores
- To connect to the VM using the Microsoft Remote Desktop, you'll need the IP address of the VM, which you can get by running the command `multipass info ubuntu2004`
- Once setup, follow Native installation options

## Native Installation [Unsupported]

- Installation script: You can provide an installation script that guides students through the process of installing Linux and the necessary software natively on their own machines.

```bash
#!/bin/bash

# System setup
echo "Update"
yes | sudo apt-get update

echo "Upgrade"
yes | sudo apt-get upgrade

echo "Installing Terminator"
yes | sudo apt install terminator

echo "Installing tmux"
yes | sudo apt-get install tmux

echo "Setting up SSH Server, net tools, GIT"
yes | sudo apt-get install openssh-server net-tools git htop

echo "Github Credential Save"
git config --global credential.helper store

echo "Installing Gparted"
yes | sudo apt-get install gparted

echo "Installing pip and other python packages"
yes | sudo apt install python3-pip 
yes | pip3 install opencv-python
yes | pip3 install numpy
yes | pip3 install matplotlib
yes | pip3 install pandas
yes | pip3 install opencv-contrib-python
yes | pip3 install scipy
yes | pip3 install open3d timm
yes | pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu

echo "Installing VSCode"
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
yes | sudo install -o root -g root -m 644 packages.microsoft.gpg /etc/apt/trusted.gpg.d/
sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/trusted.gpg.d/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'
rm -f packages.microsoft.gpg
yes | sudo apt install apt-transport-https
sudo apt-get update
yes | sudo apt install code # or code-insiders

echo "Installing ROS Noetic"
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
yes | sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
sudo apt-get update
yes | sudo apt install ros-noetic-desktop-full
sudo apt-get install -y ros-noetic-navigation ros-noetic-teb-local-planner* ros-noetic-ros-control ros-noetic-ros-controllers ros-noetic-gazebo-ros-control ros-noetic-ackermann-msgs ros-noetic-serial 
sudo apt-get install -y ros-noetic-turtlebot3*
sudo apt-get install -y ros-noetic-rosserial*
sudo apt-get install -y ros-noetic-rosbridge-server ros-noetic-foxglove-bridge
sudo apt-get install -y ros-noetic-laser-scan-matcher ros-noetic-amcl ros-noetic-hector-slam ros-noetic-rqt-multiplot 

sudo pip3 install -U catkin_tools

echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc

mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin build

# download the latest audubon unity package
mkdir -p src/audubon_unity
cd src/audubon_unity
git clone https://github.com/SmitRajguru/UB_CSE468_568_audubon_unity.git
if [ ! -f "config/map.yaml" ]; then
    cp UB_CSE468_568_audubon_unity/config/map.yaml ./config/map.yaml
fi
rsync -av --exclude='map.yaml' UB_CSE468_568_audubon_unity/* ./
rm -rf UB_CSE468_568_audubon_unity
chmod +x script/*
chmod +x src/*

catkin build

```

<!-- <aside>
💡 Additionally follow the instructions of this Git Repo : [CSE 468/568 - Simulator](https://github.com/droneslab/audubon_gazebo/tree/cse4568)

</aside> -->

## Additional Resources

- **Programming Practice**
    - **CSV Handling**:
        - [Write up Page](https://liberating-dash-9ac.notion.site/Activity-2-Python-CSV-handling-c183888908c240408e97586d77457c47)
        - [Files](https://buffalo.box.com/s/17j8ncbio4qkufyvxkw3iknqtqug69il)

    - **JSON Parsing**:
        - [Write up Page](https://liberating-dash-9ac.notion.site/Activity-3-Python-JSON-handling-e88ccd4617084b5fa3985567dd614918)
        - [Files](https://buffalo.box.com/s/tq87e70l1b0san4srielylxkl8oc4djz)


- **ROS Setup and Usage**:
    - ROS (Robot Operating System) is a widely used framework for robot software development. To get started with ROS, check out the official documentation and tutorials available at [http://www.ros.org/](http://www.ros.org/).
    - Additionally, you can find a variety of tutorials and guides on ROS from other sources such as [ROS Wiki](http://wiki.ros.org/), [The Construct](https://www.theconstructsim.com/ros-resources/) and [Robotics Stack Exchange](https://robotics.stackexchange.com/questions/tagged/ros).
- **Linux and Command-line Interface**:
    - [The Linux Command Line](http://linuxcommand.org/) is a comprehensive guide to the command line interface.
    - [Linux Cheat Sheet](https://www.cheatography.com/davechild/cheat-sheets/linux-command-line/) is a quick reference guide for commonly used Linux commands.
    - [The Linux Survival Guide](https://linuxsurvival.com/) is another great resource for learning Linux commands and concepts.
    - [HowtoForge](https://www.howtoforge.com/) and [Linux Handbook](https://linuxhandbook.com/) are also good resources for Linux tutorials and guides.
