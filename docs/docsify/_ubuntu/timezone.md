1. Check Current Timezone
Run the following command to see your current timezone:



```bash
timedatectl
```

2. Set Timezone to Asia/Manila
Use this command to set the timezone:

```bash
sudo timedatectl set-timezone Asia/Manila

```
3. Verify the Change
Check if the timezone is updated:

```bash
timedatectl

```
It should now display:


```bash
Time zone: Asia/Manila (PST, +08:00)

```

4. Restart Services (if necessary)
If you have applications relying on system time, restart them, e.g.:

```bash
sudo systemctl restart cron
```

