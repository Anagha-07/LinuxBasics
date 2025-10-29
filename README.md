# 🐧 Linux Commands Quick Reference

> 💡 A simple, human-friendly Linux command guide made for **beginners, learners, and interview prep**.  
> Read this before your interview, and you’ll sound like you live in the terminal 😄

---

## 📂 1️⃣ Navigation & File Management

| 🧩 Command | 🧠 Example | 💬 Explanation |
|------------|-------------|----------------|
| `pwd` | `pwd` | 📍 Show where you are (Print Working Directory). |
| `ls` | `ls -l` / `ls -a` | 📄 List files. `-l` = long list, `-a` = hidden files. |
| `cd` | `cd /home/user` | 🚶 Change Directory. |
| `cd ..` | | ⬆️ Go one folder up. |
| `mkdir` | `mkdir projects` | 🏗️ Make a new folder. |
| `rmdir` | `rmdir empty_folder` | ❌ Remove empty folder. |
| `rm -r` | `rm -r folder` | 💣 Delete folder with contents (⚠️ careful). |
| `touch` | `touch notes.txt` | 🧾 Create empty file or update timestamp. |
| `cp` | `cp file.txt /tmp/` | 🧍 Copy files (`-r` for folders). |
| `mv` | `mv file.txt new.txt` | ✏️ Move or rename file. |
| `cat` | `cat file.txt` | 📜 Show file content. |
| `less` | `less file.txt` | 👀 View large file page by page (`q` to quit). |
| `head` / `tail` | `head -n 5 file.txt` | 🔝 / 🔚 Show first or last lines. |

---

## 🧠 2️⃣ System Info & Monitoring

| Command | Meaning |
|----------|---------|
| `uname -a` | 🧩 OS & kernel info. |
| `hostname` | 🖥️ System name. |
| `whoami` | 👤 Show current user. |
| `uptime` | ⏱️ System running time. |
| `top` / `htop` | 🧠 Live process monitor. |
| `ps aux` | 🪄 List all processes. |
| `df -h` | 💾 Disk usage summary. |
| `du -sh folder/` | 📂 Folder size. |
| `free -h` | 🧮 RAM usage. |
| `history` | 🕰️ List past commands. |

---

## 🔐 3️⃣ Permissions & Ownership

| Command | Example | Meaning |
|----------|----------|---------|
| `chmod` | `chmod 755 script.sh` | 🔧 Change file permissions. |
| `chown` | `chown user:group file` | 👑 Change file owner. |

> 🧠 **r = read, w = write, x = execute**  
> Numbers: `7=rwx`, `6=rw-`, `5=r-x`, `4=r--`.

---

## 👥 4️⃣ User Management

| Command | Example | Meaning |
|----------|----------|---------|
| `who` | | 👥 See who’s logged in. |
| `id` | | 🪪 Show user & group info. |
| `sudo` | `sudo apt update` | ⚡ Run as superuser (admin). |
| `adduser` | `sudo adduser bob` | ➕ Add new user. |
| `passwd` | `passwd bob` | 🔑 Change password. |
| `deluser` | `sudo deluser bob` | 🗑️ Delete user. |

---

## 📦 5️⃣ Package Management (Ubuntu/Debian)

| Command | Meaning |
|----------|---------|
| `sudo apt update` | 🔁 Update package list. |
| `sudo apt upgrade` | 📈 Upgrade all packages. |
| `sudo apt install nginx` | 📦 Install a package. |
| `sudo apt remove nginx` | ❌ Uninstall package. |
| `dpkg -l` | 🧾 List installed packages. |

---

## 🌐 6️⃣ Networking

| Command | Example | Meaning |
|----------|----------|---------|
| `ping google.com` | | 🌍 Test connectivity. |
| `ifconfig` / `ip a` | | 🔌 Show IP addresses. |
| `netstat -tuln` | | 🔎 View open ports. |
| `curl` | `curl https://example.com` | 🌐 Fetch webpage data. |
| `wget` | `wget https://file.com` | ⬇️ Download file. |

---

## 🔥 7️⃣ UFW – Uncomplicated Firewall

| Command | Meaning |
|----------|---------|
| `sudo ufw status` | 📊 Check firewall status. |
| `sudo ufw enable` | 🟢 Turn ON firewall. |
| `sudo ufw disable` | 🔴 Turn OFF firewall. |
| `sudo ufw allow 22` | ✅ Allow SSH (port 22). |
| `sudo ufw deny 80` | 🚫 Block HTTP (port 80). |
| `sudo ufw delete allow 22` | ❌ Remove rule. |

---

## ⚙️ 8️⃣ Service Management

| Command | Meaning |
|----------|---------|
| `service --status-all` | 📋 List all services. |
| `sudo service nginx start` | ▶️ Start service. |
| `sudo service nginx stop` | ⏹️ Stop service. |
| `sudo service nginx restart` | 🔁 Restart service. |
| `sudo systemctl status nginx` | 🧠 Check detailed status (newer way). |

> 💡 `systemctl` = modern systemd tool, `service` = classic helper.

---

## 🗜️ 9️⃣ Archiving & Compression

| Command | Meaning |
|----------|---------|
| `tar -cvf file.tar folder/` | 📦 Create archive. |
| `tar -czvf file.tar.gz folder/` | 🧳 Create compressed archive. |
| `tar -xvf file.tar` | 📂 Extract archive. |
| `zip -r file.zip folder/` | 🧩 Zip folder. |
| `unzip file.zip` | 📤 Extract zip file. |

> 🧠 **c = create**, **x = extract**, **v = verbose**, **f = file**, **z = zip**

---

## 🌱 🔟 Environment Variables

| Command | Meaning |
|----------|---------|
| `printenv` | 🧾 List environment variables. |
| `export VAR=value` | 📤 Set variable globally. |
| `echo $VAR` | 📢 Show variable value. |
| `unset VAR` | ❌ Remove variable. |
| `env VAR=value command` | ⚙️ Run command with temporary variable. |

> 💡 `export` = make available to other programs/shells.

---

## 💾 11️⃣ Disk & File System

| Command | Use |
|----------|-----|
| `lsblk` | 💽 List disks. |
| `mount` / `umount` | 🔗 Mount or unmount storage. |
| `df -h` | 📊 Disk space. |
| `du -sh folder/` | 📏 Folder size. |

---

## 🔍 12️⃣ Searching & Finding

| Command | Use |
|----------|-----|
| `find . -name "*.txt"` | 🔎 Find files. |
| `grep "error" file.txt` | 📘 Search text inside file. |
| `grep -r "fail" /var/log` | 🗂️ Search recursively. |

> 🧠 grep = **G**lobal **R**egular **E**xpression **P**rint

---

## ⚙️ 13️⃣ Process Management

| Command | Meaning |
|----------|---------|
| `ps aux` | 🧾 List all processes. |
| `kill PID` | 🔪 Stop process. |
| `kill -9 PID` | 💣 Force kill process. |
| `jobs` | 🧍 View background jobs. |
| `bg` / `fg` | 🔄 Move jobs background/foreground. |

---

## 🧾 14️⃣ Permissions & Links

| Command | Meaning |
|----------|---------|
| `ln file linkname` | 🔗 Hard link (same data). |
| `ln -s file linkname` | 🪞 Soft link (shortcut). |
| `ls -i` | 🔢 Show inode numbers. |

> 🧠 *Hard link = same heart, Soft link = same face.*

---

## 🧰 15️⃣ Text Editing & VS Code Tips

| Task | Command | Meaning |
|-------|----------|---------|
| Edit file (simple) | `nano file.txt` | ✏️ Open nano editor. |
| Edit file (advanced) | `vim file.txt` | ⚙️ Use Vim editor. |
| Open folder in VS Code | `code .` | 🚀 Opens current folder in VS Code. |
| Clear terminal | `clear` or `Ctrl+L` | 🧼 Clean screen. |

---

## ⚡ 16️⃣ Useful Keyboard Shortcuts

| Shortcut | Action |
|-----------|--------|
| `Ctrl + C` | ❌ Stop running command. |
| `Ctrl + D` | 🚪 Logout / Exit shell. |
| `Ctrl + L` | 🧹 Clear terminal. |
| `↑ / ↓` | 🔁 Command history navigation. |
| `Tab` | ✨ Autocomplete commands/files. |

---

## 🧠 17️⃣ The Ubuntu Welcome Message (MOTD)

When you open Ubuntu and see this:

```

Welcome to Ubuntu 24.04.1 LTS (GNU/Linux ...)
System info, IP, disk usage...

````

That’s the **Message of the Day (MOTD)**.  
📍 It shows your system summary.  
To disable it:
```bash
touch ~/.hushlogin
````

---

## 💡 18️⃣ Must-Know Pro Tips

* 🧾 `man command` → open full manual page.
* ⚙️ `command --help` → quick summary help.
* 🕰️ `history` → check what you’ve run before.
* 🔁 `!number` → rerun command from history.
* 🛠️ Add your script folder to PATH:

  ```bash
  export PATH=$PATH:~/scripts
  ```
---

## 🚀 19️⃣ Quick Setup Shortcuts

| Task                   | Command  |
| ---------------------- | -------- |
| Open folder in VS Code | `code .` |
| Go home                | `cd ~`   |
| Go root                | `cd /`   |
| Check disk usage       | `df -h`  |
| Check IP               | `ip a`   |

---

> 💬 “Linux isn’t about memorizing commands, it’s about **understanding what’s happening**.”
> Use this README to revise before interviews or practice daily.
> With consistency, the terminal becomes second nature. ⚡

---
