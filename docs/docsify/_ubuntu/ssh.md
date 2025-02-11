
Step 1: Update Your System

```bash
sudo apt update && sudo apt upgrade -y
```
or

```bash
sudo apt install -y openssh-server
```

2. Check SSH Service Status
After installation, ensure that the SSH service is running:


```bash
sudo systemctl status ssh
```

If it is not active, start it using:


```bash
sudo systemctl start ssh
```

To enable SSH to start automatically on boot:


```bash
sudo systemctl enable ssh
```

