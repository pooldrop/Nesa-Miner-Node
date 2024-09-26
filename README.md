# Nesa-Miner-Node

Run miner node on nesa network testnet

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev -y
```
```bash
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
```bash
sudo groupadd docker
sudo usermod -aG docker $USER
```

1. Visit the [Hugging Face website](https://huggingface.co/).

2. Sign up or log in to your account.

3. Navigate to your [API access tokens page](https://huggingface.co/settings/tokens) under your account settings.

4. Click **“Create new token”**, head to **“Write”** tab, and generate an API key by clicking on **“Create token”** .

5. Copy the generated key to use it in your miner installation.

```bash
bash <(curl -s https://raw.githubusercontent.com/nesaorg/bootstrap/master/bootstrap.sh)
```

* **Select a mode**: Choose **Wizardy**.
* **Choose a Moniker**: Provide a unique name for your node.
* **Node hostname**: skip & press `Enter`.
* **Node email**: skip & press `Enter`.
* **Enter Referral Code: to get bonus points**: skip & press `Enter`.
* **Wallet Private Key**: Enter your wallet private key for miner registration and to receive rewards.
* Finalize Configuration: Review and confirm the configuration before starting your node. The bootstrap script will provide a summary of your configuration and allow you to make changes before starting the miner.

Get node status url
```bash
PUB_KEY=$(cat $HOME/.nesa/identity/node_id.id)
echo https://node.nesa.ai/nodes/$PUB_KEY
```

Check Containers: You must have 4 new containers now
```bash
docker ps
```
