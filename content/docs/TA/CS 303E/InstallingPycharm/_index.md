---
weight: 20
title: Setting up Pycharm
---

# Installing and Setting up Pycharm

---
Last Updated: macOS Catalina 10.14 | Windows 10 | Linux Ubuntu 20.04


My preferred IDE (Integrated Development Environment) for programming in Python is [PyCharm](https://www.jetbrains.com/pycharm/). Make sure to have [Python](https://www.python.org/downloads/) installed before installing PyCharm so we can properly setup your environment

{{< tabs "OS" >}}

{{< tab "MacOS" >}} 

## Install

Download the community edition .dmg file from https://www.jetbrains.com/pycharm/download/#section=mac and navigate to the directory you downloaded it at

Double click the .dmg to start the installation

![](/~bebeal/installing-using-pycharm/m1.png)

Drag the PyCharm CE icon to the Appliations folder icon

![](/~bebeal/installing-using-pycharm/m2.png)

Navigate to your Applications directory and open PyCharm

![](/~bebeal/installing-using-pycharm/m3.png)

---

## Setup

To setup PyCharm we first need to go through some preliminary options.

Choose whether or not you want to send data statistics

![](/~bebeal/installing-using-pycharm/m4.png)

Choose "Do not import settings" then select `OK`

![](/~bebeal/installing-using-pycharm/msetup1.png)

Choose what keymap you want (I suggest the `I've never used PyCharm`)

![](/~bebeal/installing-using-pycharm/m6_1.png)

Choose Dark or Light theme (PyCharm has custom themes you can install later on with plugins)

![](/~bebeal/installing-using-pycharm/msetup2.png)

By default, PyCharm does not provide a command-line launcher. For information about creating a launcher script for PyCharm see [here](https://www.jetbrains.com/help/pycharm/opening-files-from-command-line.html). If this doesn't apply to you then you can continue to the next step

![](/~bebeal/installing-using-pycharm/m_8.png)

If you're familiar with any of these then you can choose to install them (you can install these at anytime)

![](/~bebeal/installing-using-pycharm/msetup3.png)

In the bottom right corner select the `Configure` menu then the `Preferences` option

![](/~bebeal/installing-using-pycharm/msetup4.png)

Select `Project Interpreter` on the left then click the cog wheel in the top right and select `Add`

![](/~bebeal/installing-using-pycharm/msetup5.png)

If you installed Python already then the base interpreter path should already be linked to your Python installation. If it isn't you can click the drop down menu and navigate to wherever you installed Python at. &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; Check the `inherit global site-packages` and `Make available to all projects` options and finally press `OK`

![](/~bebeal/installing-using-pycharm/msetup6.png)

Now we can setup your project directory that will contain your Python files. 

Select `New Project`

![](/~bebeal/installing-using-pycharm/msetup7.png)

Change the name of the directory to whatever you would like, I chose `CS303E` and then select `Exisitng interpreter` and finally `Create`

![](/~bebeal/installing-using-pycharm/msetup8.png)

To create a Python file simply right click the project directory on the left and select `New` -> `Python File`

![](/~bebeal/installing-using-pycharm/msetup9.png)

Voila!

![](/~bebeal/installing-using-pycharm/msetup10.png)

{{< /tab >}}



{{< tab "Windows" >}} 

## Install

Download the community edition executable from https://www.jetbrains.com/pycharm/download/#section=windows and navigate to the directory you downloaded it at.

Double click the executable to start the installation

![](/~bebeal/installing-using-pycharm/w0.png)

Select `Next`

![](/~bebeal/installing-using-pycharm/w1.png)

You can customize the install location if you would like then select `Next`

![](/~bebeal/installing-using-pycharm/w2.png)

You can add any of these options if you'd like, I recommend at least selecting `Create Desktop Shortcut` and `Create Associations`. 

![](/~bebeal/installing-using-pycharm/w3.png)

Lastly you can choose the Start Menu Folder for the PyCharm shortcut and then select `Install`

![](/~bebeal/installing-using-pycharm/w4.png)

Check "Run PyCharm Community Edition" and select `Finish`

![](/~bebeal/installing-using-pycharm/w5.png)

---

## Setup

To setup PyCharm we first need to go through some preliminary options.

Choose "Do not import settings" then select `OK`

![](/~bebeal/installing-using-pycharm/wsetup1.png)

Choose Dark or Light theme (PyCharm has custom themes you can install later on with plugins)

![](/~bebeal/installing-using-pycharm/wsetup2.png)

If you're familiar with any of these then you can choose to install them (you can install these at anytime)

![](/~bebeal/installing-using-pycharm/wsetup3.png)

In the bottom right corner select the `Configure` menu then the `Settings` option

![](/~bebeal/installing-using-pycharm/wsetup4.png)

Select `Project Interpreter` on the left then click the cog wheel in the top right and select `Add`

![](/~bebeal/installing-using-pycharm/wsetup5.png)

If you installed Python already then the base interpreter path should already be linked to your Python installation. If it isn't you can click the drop down menu and navigate to wherever you installed Python at. &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; Check the `inherit global site-packages` and `Make available to all projects` options and finally press `OK`

![](/~bebeal/installing-using-pycharm/wsetup6.png)

Now we can setup your project directory that will contain your Python files. 

Select `New Project`

![](/~bebeal/installing-using-pycharm/wsetup7.png)

Change the name to whatever you would like, I chose `CS303E` and then select `Exisitng interpreter` and finally `Create`

![](/~bebeal/installing-using-pycharm/wsetup8.png)

To create a Python file simply right click the project directory on the left and select `New` -> `Python File`

![](/~bebeal/installing-using-pycharm/wsetup9.png)

Voila!

![](/~bebeal/installing-using-pycharm/wsetup10.png)

{{< /tab >}}



{{< tab "Linux" >}} 

## Install 

You have two main options for installing PyCharm you can either use snap packages or tar archives.

<h4>Snap</h4> 

For Ubuntu 16.04 and later, you can use snap packages to install PyCharm. Open up a terminal and run
```bash
sudo snap install pycharm-community --classic
```

Open up PyCharm from the Applications Dock

![](/~bebeal/installing-using-pycharm/l3.png)

---

<h4>Tar Archives</h4>

Download the community edition tarball from https://www.jetbrains.com/pycharm/download/#section=linux and navigate to the directory you downloaded it at.

The recommended installation location for applications according to the filesystem hierarchy standard (FHS) is /opt. To install PyCharm into this directory, enter the following command:

```bash
sudo tar xzf pycharm-*.tar.gz -C /opt/
```

Switch to the bin subdirectory

```bash
cd /opt/pycharm-*/bin
```

![](/~bebeal/installing-using-pycharm/l1.png)

Run pycharm.sh from the bin subdirectory and continue to the Setup step. (We will create a Desktop Entry later so that you don't have to run this command from the terminal everytime)

```bash
sh pycharm.sh
```

---

## Setup

Before we setup PyCharm you need to install a distutils python package. Open a terminal and run

```bash
sudo apt-get install python3-distutils
```

To setup PyCharm we first need to go through some preliminary options.

Choose whether or not you want to send data statistics

![](/~bebeal/installing-using-pycharm/l4.png)

Choose Dark or Light theme (PyCharm has custom themes you can install later on with plugins)

![](/~bebeal/installing-using-pycharm/l5.png)

If you're familiar with any of these then you can choose to install them (you can install these at anytime)

![](/~bebeal/installing-using-pycharm/l6.png)

{{< details "Create Desktop Entry" >}}

If you installed PyCharm through the Tar Archives then you should create a Desktop Entry for easier access. In the bottom right corner select the `Configure` meny then the `Create Desktop Entry` option.

![](/~bebeal/installing-using-pycharm/l2.png)

{{< /details >}}

In the bottom right corner select the `Configure` menu then the `Settings` option

![](/~bebeal/installing-using-pycharm/l7.png)

Select `Project Interpreter` on the left then click the cog wheel in the top right and select `Add`

![](/~bebeal/installing-using-pycharm/l8.png)

If you installed Python already then the base interpreter path should already be linked to your Python installation. If it isn't you can click the drop down menu and navigate to wherever you installed Python at. &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; Check the `inherit global site-packages` and `Make available to all projects` options and finally press `OK`

![](/~bebeal/installing-using-pycharm/l9.png)

Now we can setup your project directory that will contain your Python files. 

Select `New Project`

![](/~bebeal/installing-using-pycharm/l12.png)

Change the name to whatever you would like, I chose `CS303E` and then select `Exisitng interpreter` and finally `Create`

![](/~bebeal/installing-using-pycharm/l13.png)

To create a Python file simply right click the project directory on the left and select `New` -> `Python File`

![](/~bebeal/installing-using-pycharm/l14.png)

Voila!

![](/~bebeal/installing-using-pycharm/l15.png)

{{< /tab >}}



{{< /tabs >}}