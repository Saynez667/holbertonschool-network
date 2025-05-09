 Network Basics Project - Part 2 🌐🖥️

Welcome to the second part of the Network Basics Project! This section focuses on understanding localhost, IP addresses, the hosts file, and practical networking tools like netcat.

---

## 🚀 Project Overview

This project covers:

- What **localhost** and **127.0.0.1** mean
- The significance of **0.0.0.0**
- Understanding the **/etc/hosts** file and how it maps hostnames to IP addresses
- How to display your machine’s active network interfaces
- Using **netcat (nc)** for listening on ports and network debugging

You will write Bash scripts to modify hostname resolution, display IPs, and listen on ports locally.

---

## 📚 Learning Objectives

By the end of this project, you will be able to explain:

- What **localhost** and the IP `127.0.0.1` represent (the loopback address for the local machine)
- What **0.0.0.0** means (a non-routable meta-address used to designate an invalid, unknown, or non-applicable target)
- The purpose and usage of the **/etc/hosts** file (local hostname to IP address mappings)
- How to display all active IPv4 addresses on your machine
- How to create a TCP listener on a specific port using Bash and netcat

---

## 📝 Project Requirements

- Allowed editors: `vi`, `vim`, `emacs`
- Scripts must run on **Ubuntu 22.04**
- All files must end with a newline
- All Bash scripts must be executable
- Scripts must pass **Shellcheck** (version 0.7.0) without errors
- Each script must start with:
#!/usr/bin/env bash

Comment explaining what the script does
text
- A `README.md` file is mandatory at the root of the project folder

---

## 📂 Project Tasks

| Task | Filename                    | Description                                            |
|-------|-----------------------------|--------------------------------------------------------|
| 0     | `0-change_your_home_IP`      | Modify `/etc/hosts` so localhost resolves to 127.0.0.2 and facebook.com to 8.8.8.8 |
| 1     | `1-show_attached_IPs`        | Display all active IPv4 IP addresses on the machine    |
| 2     | `2-port_listening_on_localhost` | Create a TCP listener on port 98 on localhost using netcat |

---

## 💡 Key Concepts

### Localhost and 127.0.0.1
- **Localhost** refers to the current machine making a network request to itself.
- The IP address **127.0.0.1** is reserved for loopback network interfaces.
- When you ping localhost, you are pinging your own machine.

### 0.0.0.0
- Represents all IPv4 addresses on the local machine.
- Used to specify "any address" when binding network services.
- Not routable on the internet.

### /etc/hosts file
- A local file that maps hostnames to IP addresses.
- Overrides DNS lookups for the specified hostnames.
- Useful for testing or overriding domain resolutions locally.

### Displaying IP addresses
- Tools like `ip`, `ifconfig`, or `hostname -I` can show active network interfaces and their IPs.
- Example command to get IPv4 addresses excluding loopback:
ip -4 addr show scope global | grep inet | awk '{print $2}' | cut -d/ -f1


### Netcat (nc)
- A versatile networking tool used to listen on ports, send data, scan ports, and debug networks.
- Can be used to create a simple TCP listener on a port.
- Example to listen on port 98:
nc -l 98

---

## 🎯 How to Use

1. Run `0-change_your_home_IP` script to update hostname resolutions.
2. Use `1-show_attached_IPs` to list all active IPv4 addresses on your machine.
3. Run `2-port_listening_on_localhost` to listen on TCP port 98 on localhost.
4. Connect to port 98 using `telnet localhost 98` from another terminal to test.

---

## ⚠️ Important Notes

- Changing localhost IP in `/etc/hosts` can affect system behavior; revert changes if needed.
- Netcat implementations vary; some flags differ between BSD and GNU versions.
- Ensure you have necessary permissions (e.g., run scripts with `sudo` if required).

## Author
- [Saynez667](https://github.com/Saynez667)