# 🐧 Linux User & Permission Management — Help Desk Ticket Simulation

This project simulates a real-world Help Desk ticket where I performed essential **Linux system administration** tasks on an Ubuntu host. The core goal was to implement strong user management, enforce password policies, and secure a sensitive directory following the **principle of least privilege**. This reflects common tasks performed by junior IT Support, SysAdmin, or SOC analysts.

---

## 📌 Project Overview

This simulation covered critical Linux security and administration concepts:

* **Adding and managing** Linux user accounts
* **Enforcing** strong password policies
* **Creating and securing** a sensitive directory
* Applying proper **permissions and Access Control Lists (ACLs)**
* Adhering to the **principle of least privilege**

---

## 📝 Ticket Requirements

The specific tasks requested in the simulated ticket were:

* Add two new users: **Bertram** and **Erlich**
* Set **temporary passwords** for both
* **Enforce password change** at first login
* Create the `Confidential` directory
* Set **`root` as the owner** for `Confidential`
* Grant **full access** (`rwx`) to **Bertram** and **Erlich**
* **Deny access** to all other system users

---

## 🧩 Steps I Completed

I used standard Linux command-line utilities to meet all ticket requirements.

### 1. User Creation and Password Policy Enforcement

| Step | Command | Purpose |
| :--- | :--- | :--- |
| **1. Created the users** | `sudo adduser Bertram` | Adds the new user account **Bertram**. |
| | `sudo adduser Erlich` | Adds the new user account **Erlich**. |
| **2. Set temporary passwords** | `sudo passwd Bertram` | Sets the initial, temporary password. |
| | `sudo passwd Erlich` | Sets the initial, temporary password. |
| ![Created users with password]() |
| **3. Enforced password reset at first login** | `sudo chage -d 0 Bertram` | Sets the **last password change date** to **0** (Epoch), forcing the user to change their password immediately upon their first successful login. |
| | `sudo chage -d 0 Erlich` | Applies the same password reset enforcement to **Erlich**. |
| ![Enforced password reset]() |

### 2. Directory Creation and Security Configuration

| Step | Command | Purpose |
| :--- | :--- | :--- |
| **4. Created the /Confidential directory** | `sudo mkdir /Confidential` | Creates the new sensitive directory. |
| **5. Set secure ownership** | `sudo chown root:root /Confidential` | Ensures the directory is owned by the **`root` user and `root` group**, maintaining central control. |
| **6. Locked down permissions to root only** | `sudo chmod 700 /Confidential` | Sets the base permissions to **read, write, and execute for the owner (`root`) only**. This denies all access to group members and all other users by default. |
| ![Directory_created_with_lock_down_permission_to_root_only_and_with_secured_ownership]() |

---

## 🎓 What I Learned

This project reinforced several key concepts essential for system administration and security:

* **Linux User & Account Management**
    * Creating users with `adduser` and setting passwords with `passwd`.
    * Enforcing password resets with the `chage -d 0` command.
* **File System Security**
    * Managing ownership with `chown`.
    * Controlling base permissions with `chmod`.
* **Security Best Practices**
    * Successfully implementing the **Principle of Least Privilege** by granting specific access only to the required users.
    * Securing sensitive directories with restrictive default permissions.
* **Help Desk Workflow**
    * Reading, interpreting, and accurately executing multi-step ticket requirements.
    * The importance of **documenting and verifying** all configuration changes.
