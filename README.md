# 🛠️ Practical Help Desk Ticket (Linux User & Group Management)

## 📌 Project Overview

This project simulates a real Help Desk ticket that required adding new Linux users, enforcing password resets, and configuring secure access to a confidential directory using only standard Linux user/group and permission commands.
This task demonstrates core Linux administration skills that are essential for IT Support, SysAdmin, and Security roles.

## 📝 Ticket Requirements

* **Create two new users:** Bertram and Erlich
* **Force both users** to change their passwords on next login
* **Create a secure directory** accessible only by a specific group
* **Create a group** named confidential
* **Add both users** to the group
* **Restrict directory permissions** so that only the group and root can access it

## 🧩 Steps I Completed 
### 1️⃣ **Create the users**
bash
'''
sudo adduser Bertram
sudo adduser Erlich
'''