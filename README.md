
# My important notes

## Creating an ssh key "id_ed25519"

` ssh-keygen -t ed25519 -C "your_email@example.com" `

- follow along the instructions

## Connecting to our remote machine or local VM

- start our ssh-agent

` eval "$(ssh-agent -s)" `

- add our ssh private key

` ssh-add <"Location_Of_The_File"> `

### to use on GitHub

- ref: [Click Link](https://docs.github.com/en/enterprise-server@3.3/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
- to connect to our github with our private key

` ssh -T git@github.com `

### to use on other virtual or cloud machines/computer

- to connect to a remote server

` ssh root@<"Public_IP_Address"> `

## Installing VScode on Linux

- ref: [Click Link](https://www.makeuseof.com/how-to-install-visual-studio-code-ubuntu/)
- you can write this down in one line if you're a power user

` sudo apt update && sudo apt upgrade -y `

- now we will install the necessary dependencies for our installer repository

` sudo apt install software-properties-common apt-transport-https wget `

- we use ` wget ` for us to import Microsoft's GPG key here

` wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add - `

- now to Enable our VScode installer repository

` sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" `

- and finally to Install our enabled installer repo

` sudo apt install code `

## Installing Node for Linux (Ubuntu)

- ref: [Click Link](https://github.com/nodesource/distributions/blob/master/README.md)
- to install "Node.js v17.x"

### as Ubuntu sudoer

`curl -fsSL https://deb.nodesource.com/setup_17.x | sudo -E bash -`

`sudo apt-get install -y nodejs`

### as Debian root

`curl -fsSL https://deb.nodesource.com/setup_17.x | bash -`

`apt-get install -y nodejs`

## Installing Chrome using Ubuntu terminal

- we get the package

`wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb`

- and install it using "dpkg" or depackage method

`sudo dpkg -i google-chrome-stable_current_amd64.deb`
