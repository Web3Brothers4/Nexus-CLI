<h2 align=center>Run Nexus Prover Beta</h2>

## Info

- You need to have min 4 RAM in your system (VPS)
- Recommended : 6 GB RAM
- You can buy VPS from [PQ Hosting or CONTABO]

---

This script is compatible with Ubuntu on local system as well as on VPS

- If you run on VPS, u don't need to do anything after running the installation commands
- If you run on Local system (Ubuntu), u just need to open the terminal after turning on your system to start this prover, it will start running automatically again, if it is not running then use this command to run

```bash
sudo systemctl start nexus.service
```

## Installation

- You can use either this command

```bash
sudo apt install curl && curl -sSL https://raw.githubusercontent.com/zunxbt/nexus-prover/main/nexus.sh | bash
```

- Or this command to run this script

```bash
sudo apt install wget && wget -qO - https://raw.githubusercontent.com/zunxbt/nexus-prover/main/nexus.sh | bash
```

## Status

- You can check prover status using this command

```bash
systemctl status nexus.service
```

- To check logs, use the below command

```bash
journalctl -u nexus.service -f -n 50
```

- Now open terminal and use the below command

```bash
sed -i 's/.*/YOUR_PROVER_ID/' .nexus/prover-id
```

- Make sure to replace `YOUR_PROVER_ID` with the value u copied earlier (Example : `sed -i 's/.*/P2Fn8XlXjuWr8yeoJvE6bi2iP1I3/' .nexus/prover-id`)
- Now restart the nexus.service using below command

```bash
  sudo systemctl restart nexus.service
```

- After some times, u will see that, your CLI nexus points will also be displayed on [Nexus Beta Website](https://beta.nexus.xyz/) upon clicking `Profile` section
