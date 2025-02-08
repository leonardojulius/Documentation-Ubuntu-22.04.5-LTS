## Step 1: Update Your System

Run the following commands to update your system:

```bash
sudo apt update && sudo apt upgrade -y
```

## 2. Install Required Dependencies
Ensure you have the necessary packages installed:

```bash
sudo apt install curl zip unzip git -y
```

## 3. Check Your Current PHP Version

```bash
php -v
```
## 4. Add the PHP PPA Repository
Ubuntu 22.04’s default repo may not have the latest PHP versions. Add the Ondrej PPA (a trusted source for PHP versions):

```bash
sudo add-apt-repository ppa:ondrej/php -y
sudo apt update
```

## 5. Install PHP 8.2 and Required Extensions
Run the following command to install PHP 8.2 and common extensions used in Laravel:

```bash
sudo apt install php8.2 php8.2-cli php8.2-mbstring php8.2-xml php8.2-bcmath php8.2-curl php8.2-zip php8.2-tokenizer php8.2-intl php8.2-sqlite3 php8.2-mysql -y
```

## 6. Verify PHP Version

```bash
php -v
```