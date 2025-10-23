# Nextcloud CLI Installation Guide
**When Web Installer Fails - The Nuclear Option**

## 🎯 When to Use This Method

**Use the CLI installer if:**
- ✅ Web installer form "blinks" without progress
- ✅ No error messages appear in browser
- ✅ Database connection works (tested with `mysql -u nextclouduser -p`)
- ✅ File permissions are correct (checked with `ls -la`)
- ✅ Apache logs show no errors
- ✅ You've spent more than 4-6 hours debugging the web installer

**Don't waste time debugging the web installer endlessly - bypass it!**

---

## 📋 Prerequisites

Before running this method, verify:

### 1. Apache is Running
```bash
sudo systemctl status apache2
```
Should show "active (running)"

### 2. Database Exists and User Works
```bash
sudo mysql -u nextclouduser -p nextcloud
```
Should connect successfully. Type `EXIT;` when done.

### 3. PHP is Installed
```bash
php -v
```
Should show PHP 8.x

### 4. Nextcloud Files Exist
```bash
ls /var/www/nextcloud/
```
Should show folders: apps, config, core, etc.

### 5. Permissions are Correct
```bash
sudo chown -R www-data:www-data /var/www/nextcloud
sudo chmod -R 755 /var/www/nextcloud
```

---

## ⚡ CLI Installation Method

### Step 1: Navigate to Nextcloud Directory
```bash
cd /var/www/nextcloud
```

### Step 2: Run CLI Installer

**Replace these values:**
- `YOUR_DB_PASSWORD` - Your nextclouduser database password
- `YOUR_ADMIN_PASSWORD` - Choose a strong admin password (save it!)

```bash
sudo -u www-data php occ maintenance:install \
  --database "mysql" \
  --database-name "nextcloud" \
  --database-user "nextclouduser" \
  --database-pass "YOUR_DB_PASSWORD" \
  --admin-user "admin" \
  --admin-pass "YOUR_ADMIN_PASSWORD"
```

### Step 3: Configure Trusted Domains

After installation, add your server IP to trusted domains:

```bash
sudo -u www-data php occ config:system:set trusted_domains 1 --value=YOUR_SERVER_IP
```

Replace `YOUR_SERVER_IP` with your actual IP (e.g., 192.168.12.128)

### Step 4: Verify Installation

```bash
sudo -u www-data php occ status
```

Should show:
```
- installed: true
- version: 29.0.x
- versionstring: 29.0.x
```

---

## 🌐 Access Your Nextcloud

Open browser and go to: `http://YOUR_SERVER_IP`

**Login with:**
- Username: `admin`
- Password: (the admin password you set in Step 2)

---

## 🔧 Common Issues and Fixes

### Issue: "Command not found: occ"
**Solution:** You're not in the right directory
```bash
cd /var/www/nextcloud
ls -la occ  # Should show the occ file
```

### Issue: "Permission denied"
**Solution:** Run with `sudo -u www-data`
```bash
sudo -u www-data php occ maintenance:install ...
```

### Issue: "Database connection failed"
**Solution:** Verify database password
```bash
sudo mysql -u nextclouduser -p nextcloud
# If this fails, your database password is wrong
```

### Issue: "Could not create config directory"
**Solution:** Fix permissions
```bash
sudo chown -R www-data:www-data /var/www/nextcloud
sudo chmod -R 755 /var/www/nextcloud
```

---

## 📊 Why CLI Install Works When Web Install Fails

### Web Installer Issues:
- ❌ JavaScript errors from browser extensions
- ❌ Browser caching old pages
- ❌ AJAX request failures
- ❌ Timeouts on slow connections
- ❌ Silent failures without error messages

### CLI Installer Advantages:
- ✅ Direct PHP execution (no browser involved)
- ✅ Clear error messages in terminal
- ✅ No JavaScript/AJAX/browser dependencies
- ✅ Works with any firewall/network configuration
- ✅ Same exact result as web installer

---

## 🎓 Lessons Learned

### **Pivot Early, Not Late**

**Bad approach:**
- Spend 24 hours debugging one method
- Try the same thing repeatedly
- Hope it will eventually work

**Good approach:**
- Debug for 4-6 hours maximum
- If blocked, ask: "Is there another way?"
- Try alternative methods
- Value results over method

### **Know Your Tools**

Every major application has multiple installation methods:
- Web installer (GUI)
- CLI installer (command line)
- Configuration files (manual)
- APIs (programmatic)

**When one fails, use another.**

---

## 🚀 Next Steps After Installation

### 1. Install Essential Apps
```bash
sudo -u www-data php occ app:install files_external
sudo -u www-data php occ app:install calendar
sudo -u www-data php occ app:install contacts
sudo -u www-data php occ app:install tasks
```

Or use the web interface: Profile icon → Apps

### 2. Create Additional Users
```bash
sudo -u www-data php occ user:add USERNAME
```

Or use web interface: Profile icon → Users

### 3. Configure Email (Optional)
```bash
sudo -u www-data php occ config:system:set mail_smtpmode --value="smtp"
sudo -u www-data php occ config:system:set mail_from_address --value="nextcloud"
sudo -u www-data php occ config:system:set mail_domain --value="yourdomain.com"
```

### 4. Set Up Cron Job
```bash
sudo crontab -u www-data -e
```

Add this line:
```
*/5 * * * * php -f /var/www/nextcloud/cron.php
```

### 5. Security Hardening (Next Phase)
- Set up HTTPS with Let's Encrypt
- Configure fail2ban
- Enable two-factor authentication
- Set up automated backups

---

## 📚 Additional Resources

**Official Nextcloud Documentation:**
- CLI Installation: https://docs.nextcloud.com/server/latest/admin_manual/installation/command_line_installation.html
- OCC Commands: https://docs.nextcloud.com/server/latest/admin_manual/configuration_server/occ_command.html

**Troubleshooting:**
- Check logs: `sudo tail -f /var/www/nextcloud/data/nextcloud.log`
- Apache logs: `sudo tail -f /var/log/apache2/error.log`
- System status: `sudo -u www-data php occ status`

---

## 🎯 Summary

**When web installer fails after basic troubleshooting:**

1. Don't keep trying the same thing
2. Switch to CLI installer immediately
3. Get the system working
4. Document what happened
5. Move forward with your project

**Time saved by using CLI from the start: 20+ hours**

---

*This guide is part of the Green AI Lab project - building enterprise cloud infrastructure from e-waste hardware.*