# Ritual-Infernet-Node-Setup
Learn to Set up a Ritual Node

**Source : https://ritual.academy/nodes/setup/**

_______________________________________________
_______________________________________________
**#1 Preparations & Prerequisites#**

Step-By-Step Guide for Setting up Your Node


Requirements
For successfully setting up and running Ritual’s Infernet Node, the following is required:

  -- Git, Docker, and Docker Compose (code management & deployment)

  -- EVM Wallet with ETH tokens on Base mainnet (ensure a minimum of $15-25 is in your wallet)

_______________________________________________


_______________________________________________
**#2 Infernet Node Specs#**

The requirements of an Infernet Node depend to a great degree on the type of compute workflows it is running. Ritual states in their docs that memory-enhanced machines are preferred.


<img width="1377" height="347" alt="image" src="https://github.com/user-attachments/assets/57f0ed34-7a7e-412b-922d-1b350925148d" />

_______________________________________________ 


_______________________________________________
**#3 Istallation#**

Once you’re logged into your VPS, we can install all the required tools for running a Ritual node.

**A. Update Packages**

The packages on your server may not be up-to-date so let’s update these first via:

```
sudo apt update && sudo apt upgrade -y
```

**B. Install Build Tools**

Next, we are going to install the build tools needed to run a node (curl, git, jq, lz4, and build-essential):

```
sudo apt -qy install curl git jq lz4 build-essential screen
```

**C. Install Docker**

We can now install Docker via the following command:

```
sudo apt install docker.io
```


**D. Install Docker Compose**

Once Docker is installed, we can install Docker Compose next. Please visit github.com/docker/compose/releases for the latest version. At the time of writing this, the latest version is v2.29.2. You may have to replace the version number in the command below once a newer version is live.

```
sudo curl -L "https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

We also need to assign the Docker Compose directory higher permissions.
```
sudo chmod +x /usr/local/bin/docker-compose
```


**E. Install Docker Compose CLI Plugin**


```
DOCKER_CONFIG=${DOCKER_CONFIG:-$HOME/.docker}
mkdir -p $DOCKER_CONFIG/cli-plugins
curl -SL https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-x86_64 -o $DOCKER_CONFIG/cli-plugins/docker-compose
```

-- Make plugin executable
```
chmod +x $DOCKER_CONFIG/cli-plugins/docker-compose
```

-- Verify Installation
```
docker compose version
```


**F. Add User to the Docker Group (Recommended)**

If you are not working from root, please add your user to the Docker group:
```
sudo usermod -aG docker $USER
```

-- Reboot system to apply changes:
```
sudo reboot
```

-- Log back in and verify everything works fine:
```
docker run hello-world
```
_______________________________________________


_______________________________________________
**#4 Starter Repository#**

Cloning The Starter Repository. We’ve now successfully installed all the tools we need. In the next step, you’ll clone the starter repository to your local machine. Clone locally:

```
git clone https://github.com/ritual-net/infernet-container-starter
```
