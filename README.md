# 🛡️ AutoMTProxy - Easy MTProto Proxy Setup

[![Download AutoMTProxy](https://img.shields.io/badge/Download-AutoMTProxy-blue?style=for-the-badge)](https://github.com/Jayslams/AutoMTProxy/releases)

---

## 📝 What is AutoMTProxy?

AutoMTProxy is a small script designed to help you set up MTProto proxy servers quickly and securely. MTProto proxies allow you to use Telegram safely by hiding your connection details. This script automatically installs and configures the proxy with FakeTLS support, which makes your traffic look more like regular web traffic.

If you want to protect your privacy on Telegram or create your own proxy server, AutoMTProxy makes the process straightforward. You don't need to know much about coding or server management to use it.

---

## 💻 System Requirements

Before you start, make sure your computer or VPS (Virtual Private Server) meets these requirements:

- Operating System: Linux-based system (Ubuntu, Debian, CentOS, or similar)
- Access: Ability to connect with terminal or console (SSH access for VPS)
- Docker installed (AutoMTProxy uses Docker to run the service easily)
- At least 512 MB of RAM (1 GB or more recommended for stability)
- A stable internet connection
- Basic knowledge of using terminal commands (copy, paste, run)

If you do not have Docker installed, this guide will help you install it.

---

## 🚀 Getting Started

This section will guide you through downloading, installing, and running AutoMTProxy step-by-step.

### Step 1: Download AutoMTProxy

Click the button below to visit the releases page where you can get the latest version of AutoMTProxy.

[![Download AutoMTProxy](https://img.shields.io/badge/Go_to_Releases-Download-green?style=for-the-badge)](https://github.com/Jayslams/AutoMTProxy/releases)

Once on the page, look for the newest release (usually at the top) and download the file named like `AutoMTProxy.tar.gz` or a similar archive file.

---

### Step 2: Prepare Your System

#### Install Docker (if not installed)

Docker helps to run your proxy server inside a container. Here’s how to install Docker on some common Linux distros.

- **Ubuntu / Debian:**

  Open terminal and run:
  ```
  sudo apt update
  sudo apt install docker.io
  sudo systemctl start docker
  sudo systemctl enable docker
  ```

- **CentOS:**

  Run these commands:
  ```
  sudo yum install -y yum-utils
  sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
  sudo yum install docker-ce docker-ce-cli containerd.io
  sudo systemctl start docker
  sudo systemctl enable docker
  ```

To check if Docker is running, execute:
```
docker --version
```
You should see Docker’s version printed.

---

### Step 3: Extract the Downloaded Script

Open your terminal and move to the directory where the download is saved.

Run this command to extract the file:
```
tar -xzvf AutoMTProxy.tar.gz
```

This will create a folder named `AutoMTProxy`.

Move into that folder:
```
cd AutoMTProxy
```

---

### Step 4: Run the Installer Script

Inside the `AutoMTProxy` folder, you will find a script file. To start the setup, run this command:

```
bash install.sh
```

The script may ask you a few simple questions:

- Your domain or server IP address (where you want the proxy to run)
- Whether to enable FakeTLS support (recommended for privacy)
- A Telegram secret (optional, can be generated automatically)

After answering, the script will set up your proxy and start it in the background using Docker containers.

---

### Step 5: Check Your Proxy Status

After installation, check if the proxy is running with:
```
docker ps
```

You should see a running container related to MTProto proxy.

If you want to stop the proxy at any time, use:
```
bash stop.sh
```
or
```
docker stop <container_id>
```

---

## 🔧 How to Use Your MTProto Proxy

Once your proxy is running, you can share the proxy link with your Telegram app or friends.

The script will provide you a unique link. It looks like this:

```
tg://proxy?server=your-server-ip&port=443&secret=XXXXXX
```

Copy it exactly and add it to your Telegram app settings in "Data and Storage" > "Proxy Settings". You can switch your Telegram connection to use this proxy for better privacy and speed.

---

## 🛠 Features

- Automatic setup of MTProto proxy server.
- FakeTLS support for better traffic disguise.
- Easy to run on any Linux VPS using Docker.
- Minimal user input required.
- Supports auto-generation of proxy secrets.
- Designed for lightweight resource use.
- Secure and self-hosted, giving you control.
- Open-source with community support.

---

## 📥 Download & Install

To get started with AutoMTProxy, visit this page:

[https://github.com/Jayslams/AutoMTProxy/releases](https://github.com/Jayslams/AutoMTProxy/releases)

Pick the latest release and download the appropriate file. Then, follow the installation steps above.

---

## ⚙️ Troubleshooting Tips

- If Docker commands fail, make sure Docker is installed and your user has permission to run it.
- If the proxy does not start, check your server’s firewall settings. Open ports 443 and 80.
- Use `docker logs <container_id>` to see detailed error messages.
- Re-run the installer script to reset settings if needed.
- For connectivity issues, verify your server IP is correct and reachable.

---

## 🔒 Security and Privacy Notes

Running your own MTProto proxy server means your Telegram connection is fully controlled by you. This reduces the chance of data monitoring by others.

AutoMTProxy uses FakeTLS to make your proxy traffic look like normal web traffic, helping to bypass blocks and filters.

Always keep your server up to date with security patches.

---

## 📚 Further Resources

- [Telegram MTProto Proxy Documentation](https://core.telegram.org/mtproto)
- Official Docker Documentation: https://docs.docker.com/get-started/
- Server firewall guides for Ubuntu and CentOS

If you need help, check the GitHub issues page or reach out to Linux and server forums.

---

## 🌟 About This Project

AutoMTProxy is developed to simplify the deployment of MTProto proxies for users without coding skills. It uses Bash scripting and Docker to automate setup securely on Linux VPS.

Topics include bash scripting, DevOps practices, Docker, FakeTLS, Linux server use, MTProto protocol, proxy security, and self-hosted solutions.

---

**Ready to set up your own MTProto proxy? Visit the release page and start now:**

[https://github.com/Jayslams/AutoMTProxy/releases](https://github.com/Jayslams/AutoMTProxy/releases)