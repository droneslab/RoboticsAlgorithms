---
layout: page
title: Resources
description: Resources for the course.
---

# Development Environment

## Virtual Machine options

- Use one of options for Hypervisors given below or setup natively
- VMs are provided for VirtualBox and Parallels
- Credentials:
    - Username : `cse4568`
    - Password : `cse4568` (for VirtualBox)
    - Password : `cse4568` (for Parallels)
- Note : Multipass is an alternative to using VirtualBox and Parallels (which is paid) and requires more work so limited support will be available from instructors

### VirtualBox [Recommended] for x86

This is a free and open-source virtualization software that can be used to run virtual machines.

- [Oracle VM VirtualBox](https://www.virtualbox.org/)
    
- After downloading VirtualBox, install it on your machine.
- Once installed, open VirtualBox and click on the "Import" button to import a virtual machine.
- Select the pre-configured virtual machine file, this should have the extension ".ova" or ".ovf"
- Follow the prompts to import the virtual machine.
- Once imported, select the virtual machine and click on "Start" button to launch it.
- [[Pre-configured Virtual Machine download link]](https://buffalo.box.com/s/leys1fb3pgb0y24pcic9d1ztrmsbef8k)

### Parallels Desktop [Recommended] for Apple Silicon (M1x,M2x)

This is a paid virtualization software that can be used to run virtual machines.

- [Run Windows on Mac - Parallels Desktop 18 Virtual Machine for Mac](https://www.parallels.com/products/desktop/)
    
- After downloading Parallels Desktop, install it on your machine.
- Once installed, open Parallels Desktop and click on the "File" menu, select "Import".
- Select the pre-configured virtual machine file, this should have the extension ".pvm" or ".hdd"
- Follow the prompts to import the virtual machine.
- Once imported, select the virtual machine and click on "Start" button to launch it.
- [[Pre-configured Virtual Machine download link]](https://buffalo.box.com/s/28w3fogyqmpmzsirnkxun5u6qz6vnjm4)


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
## Development Environment
ges.microsoft.gpg /etc/apt/trusted.gpg.d/
sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/trusted.gpg.d/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'
rm -f packages.microsoft.gpg
yes | sudo apt install apt-transport-https
sudo apt-get update
yes | sudo apt install code # or code-insiders



echo "Installing ROS2 Humble"

locale  # check for UTF-8

sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8

locale  # verify settings

sudo apt install software-properties-common
sudo add-apt-repository universe

sudo apt update && sudo apt install curl -y
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

sudo apt update

sudo apt upgrade

sudo apt install ros-humble-desktop

sudo apt install ros-humble-ros-base

sudo apt install ros-dev-tools

# Append configurations to ~/.bashrc
{
    echo "# ROS Humble setup"
    echo "source /opt/ros/humble/setup.bash"
    echo "source /usr/share/colcon_cd/function/colcon_cd.sh"
    echo "export _colcon_cd_root=/opt/ros/humble/"
    echo "source /usr/share/colcon_argcomplete/hook/colcon-argcomplete.bash"
    echo "source /opt/ros/humble/share/ros2cli/environment/ros2-argcomplete.bash"
} >> ~/.bash_aliases

sudo apt-get install -y \
ros-humble-navigation2 \
ros-humble-nav2-dwb-controller \
ros-humble-ros2-control \
ros-humble-ros2-controllers \
ros-humble-gazebo-ros2-control \
ros-humble-ackermann-msgs \
ros-humble-foxglove-bridge \
ros-humble-pointcloud-to-laserscan \
ros-humble-slam-toolbox \
ros-humble-turtlebot3-gazebo
```

# F1tenth Edition - Deprecated

## Simulator Setup
[Link to Simulator Setup](https://liberating-dash-9ac.notion.site/F1Tenth-Simulator-Setup-5a013b6a723b490cbf6881a42a94d63f)

## VMs
- [VirtualBox [Pre-configured Virtual Machine download link]](https://buffalo.box.com/s/qedq5ph8otgbaf2cay4fzd2x01btju8e)
- [Parallels [Pre-configured Virtual Machine download link]](https://ubuffalo-my.sharepoint.com/:u:/g/personal/yashturk_buffalo_edu/EY-SkGPh42xEktLh65jzUhgBGQMxxa8Zf22FB2TuUA571g?e=DUDUxz)

<aside>
<p style="color: red; font-weight: bold;"> 💡 ROS Noetic is not installed on the VMs. This setup reuires Ununtu 20.04 (focal) </p>

</aside>


```bash
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

# Additional Resources

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
