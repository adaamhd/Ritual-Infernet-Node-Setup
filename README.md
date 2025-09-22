# Ritual-Infernet-Node-Setup
Learn to Set up a Ritual Node, source from https://ritual.academy/nodes/setup/

**Source : https://ritual.academy/nodes/setup/**


_______________________________________________
**#1 Preparations & Prerequisites**
Step-By-Step Guide for Setting up Your Node
_______________________________________________

Requirements
For successfully setting up and running Ritual’s Infernet Node, the following is required:

  -- Git, Docker, and Docker Compose (code management & deployment)

  -- EVM Wallet with ETH tokens on Base mainnet (ensure a minimum of $15-25 is in your wallet)

  
_______________________________________________
**#2 Infernet Node Specs**
The requirements of an Infernet Node depend to a great degree on the type of compute workflows it is running. Ritual states in their docs that memory-enhanced machines are preferred.
_______________________________________________

<img width="1377" height="347" alt="image" src="https://github.com/user-attachments/assets/57f0ed34-7a7e-412b-922d-1b350925148d" />

  
_______________________________________________
**#3 Istallation**
Once you’re logged into your VPS, we can install all the required tools for running a Ritual node.
_______________________________________________

**1. Update Packages**
   The packages on your server may not be up-to-date so let’s update these first via:

```
sudo apt update && sudo apt upgrade -y
```

**2. Install Build Tools**
   Next, we are going to install the build tools needed to run a node (curl, git, jq, lz4, and build-essential):

```
sudo apt -qy install curl git jq lz4 build-essential screen
```

**3. Install Docker**
   We can now install Docker via the following command:

```
sudo apt install docker.io
```


**4. Install Docker Compose**
   Once Docker is installed, we can install Docker Compose next. Please visit github.com/docker/compose/releases for the latest version. At the time of writing this, the latest version is v2.29.2. You may have to replace the version number in the command below once a newer version is live.

```
sudo curl -L "https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

We also need to assign the Docker Compose directory higher permissions.
```
sudo chmod +x /usr/local/bin/docker-compose```
