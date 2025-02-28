# Guide: [Remotely upload code from VSCode to Raspberry Pi using ssh connection](https://randomnerdtutorials.com/raspberry-pi-remote-ssh-vs-code/#:~:text=All%20you%20have%20to%20do,computer%20using%20VS%20Code%20interface.).
###  ```Hi there, I have been trying to figure out an easy way to upload the code from your own computer to Raspberry Pi remotely and this is the best way imo. Hope this can save your time setting up the connection.```
## ``STEP 1``: Make sure you **enable SSH** when imaging the SD card.
* To make sure the settings of Raspberry Pi allows you to create a ssh connection, tick ``Enable SSH`` box when **[imaging the SD card](https://projects.raspberrypi.org/en/projects/raspberry-pi-setting-up/2)** from your laptop before plugging it into the Raspberry Pi. In this stage, please remember the username and password when setting up Raspberry Pi OS.

## ``STEP 2``: Installing [Remote - SSH Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh) on VSCode .
> * The Remote - SSH extension lets you use any remote machine with a SSH server as your development environment.
> * After that, there will be an extension icon appear on the left menu bar of your VSCode, click on it to access the SSH terminal.

## ``STEP 3``: Setting up SSH connection between VSCode and Raspberry Pi.
> * To set up SSH connection from your VSCode using **[Remote - SSH Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh)**, press ``Ctrl + Shift + P`` to open the searching bar in VSCode, then find **[Remote - SSH: Add New SSH Host](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh)**.
> * Then, you will be asked to **enter SSH connection command**, in this case, type ``ssh <username>@<hostname>`` in **``STEP1``**. For example **``ssh pi@raspberrypi``**.
> * After that, select a path to store the SSH connection information. Then press ``refresh`` on the left bar to see new SSH connection under your raspberry pi host name.

## ``STEP 4``: Connecting with Raspberry Pi via SSH connection and [create virtual environment](https://learn.adafruit.com/python-virtual-environment-usage-on-raspberry-pi/basic-venv-usage).
> * Click the arrow next to your host name to access SSH connection in a new window.
> * Then, you will be asked to **select the platform of the remote host**, select Linux then type your password created in **``STEP1``**, you are now controlling Raspberry Pi via SSH.
> * You can click open folder and select the any folder or **[create a virtual environment folder on the device](https://learn.adafruit.com/python-virtual-environment-usage-on-raspberry-pi/basic-venv-usage)** if you create a new folder.
> * When you open any file in Pi from VSCode, you will be asked to enter your password again.