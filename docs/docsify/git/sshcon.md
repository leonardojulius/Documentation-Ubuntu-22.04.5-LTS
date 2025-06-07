✅ Step 1: Generate an SSH Key (if you don’t have one)
Open a terminal (can be inside VSCode) and run:

You can clone this GitHub repository using either **HTTPS** or **SSH**, depending on your preferences.


## 🚀 Step 1: Generate SSH Key

Open your terminal (either standalone or in VS Code) and run:
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"

```
💡 Replace "your_email@example.com" with your GitHub email address.


## 📁 Step 2: Add SSH Key to the SSH Agent
Start the SSH agent:

```bash
eval "$(ssh-agent -s)"

```
Add your private key to the agent:

```bash
ssh-add ~/.ssh/id_ed25519

```


## 🔐 Step 3: Copy SSH Public Key
Run the following to copy your key:

```bash
cat ~/.ssh/id_ed25519.pub

```
Copy the output that starts with ssh-ed25519.


## 🌐 Step 4: Add Key to GitHub
1.Go to GitHub SSH Keys Settings

2.Paste your copied key into the Key field

3.Add a descriptive Title (e.g., Ubuntu Laptop)

4.Click Add SSH Key

## 🧪 Step 5: Test Connection

```bash
ssh -T git@github.com

```

If successful, you’ll see:


```bash
Hi your_username! You've successfully authenticated, but GitHub does not provide shell access.

```

##   🛠  Step 6: Configure VS Code (Optional)


If using VS Code Git integration:

1. Open the command palette Ctrl+Shift+P

2. Type Remote-SSH: Open SSH Configuration File

3. Make sure your identity file points to ~/.ssh/id_ed25519

4. You can also configure it manually in ~/.ssh/config:

```bash
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519

```

✅ You're Done!
You can now clone and push GitHub repositories using SSH in VS Code.

```bash
git clone git@github.com:your_username/your_repo.git

```