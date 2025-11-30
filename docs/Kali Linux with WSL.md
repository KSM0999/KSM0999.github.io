---
layout: default
title: Kali Linux with WSL
---

1) Open a PowerShell prompt in **administrator** mode.

```PowerShell
wsl.exe --list --online
```

```PowerShell
wsl.exe --install kali-linux
```

2) Restart your computer.

3) Open a prompt in your Kali Linux.

4) Update it and install Win-Kex

```Bash
sudo apt update
```

```Bash
sudo apt install -y kali-win-kex
```

5) Create a Kali Linux GUI shortcut in your terminal

