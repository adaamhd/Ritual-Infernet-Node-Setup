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

Update Packages
The packages on your server may not be up-to-date so let’s update these first via:

<div>
<textarea class="sudo apt update && sudo apt upgrade -y">{{ copyable }}</textarea>
<p class="raw-link"><a href="{{ raw_link }}">Raw data</a></p>
</div>

<script>
var ta = document.querySelector("textarea.copyable");
var p = document.querySelector("p.raw-link");
var button = document.createElement("button");
button.className = "copyable-copy-button";
button.innerHTML = "Copy to clipboard";
button.onclick = () => {
    ta.select();
    document.execCommand("copy");
    button.innerHTML = "Copied!";
    setTimeout(() => {
        button.innerHTML = "Copy to clipboard";
    }, 1500);
};
p.appendChild(button);
p.insertAdjacentElement("afterbegin", button);
</script>



