# How to install new Node.js version in Astra Linux
---
## Step 1: download and import the Nodesource GPG key
```bash
sudo apt-get update
sudo apt-get install -y ca-certificates curl gnupg
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg
```
## Step 2: create deb repository
```bash
NODE_MAJOR=20
echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_$NODE_MAJOR.x nodistro main" | sudo tee /etc/apt/sources.list.d/nodesource.list
```
## Step 3: update apt
```bash
sudo apt-get update
```
## Step 4: install debian-keyring
```bash
sudo apt install debian-keyring
```
## Step 5: use apt-cache to find the requested nodejs version
```bash
apt-cache showpkg nodejs
Package: nodejs
Versions:
16.4.1-1nodesource1 (/var/lib/apt/lists/deb.nodesource.com_node%5f16.x_dists_stretch_main_binary-amd64_Packages)
 Description Language:
                 File: /var/lib/apt/lists/deb.nodesource.com_node%5f16.x_dists_stretch_main_binary-amd64_Packages
                  MD5: 964493985d4a02c9abd7e062f9234325
```
## Step 6: install the requested nodejs version
```bash
sudo apt install nodejs=16.4.1-1nodesource1
```
---
## Enjoy !
