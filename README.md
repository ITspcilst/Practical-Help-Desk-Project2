# 🛠️ Practical Help Desk Ticket (Linux User & Group Management)

--

## 📌 Project Overview

This project simulates a real Help Desk ticket that required adding new Linux users, enforcing password resets, and configuring secure access to a confidential directory using only standard Linux user/group and permission commands.
This task demonstrates core Linux administration skills that are essential for IT Support, SysAdmin, and Security roles.

--

## 📝 Ticket Requirements

* **Create two new users:** Bertram and Erlich
* **Force both users** to change their passwords on next login
* **Create a secure directory** accessible only by a specific group
* **Create a group** named confidential
* **Add both users** to the group
* **Restrict directory permissions** so that only the group and root can access it

--

## 🧩 Steps I Completed 
--
### 1️⃣ **Create the users**

```
sudo adduser Bertram 
sudo adduser Erlich
```
![Creating user Bretram](Screenshots/Adding_user_Bertram.png)
![Creating user Erlich](Screenshots/Adding_user_Erlich.png)

--

### 2️⃣ **Create a group named ‘confidential’**

```
sudo addgroup /confidential
```
![Creating confidential group](Screenshots/Adding_group_confidential.png)

--

### **3️⃣ Add both users to the confidential group**

```
sudo usermode -a -G 0 Bertram
sudo usermode -a -G 0 Erlich
```
![Adding users to Confidential group](Screenshots/Adding_users_to_confidential_group.png)

--

## **4️⃣ Force both users to reset their password on next login**

```
sudo chage -d 0 Bertram
sudo chage -d 0 Erlich
```
![Password reseting Bertram](Screenshots/Password_Reset_completed_Bertram.png)
![Password reseting Erlich](Screenshots/Password_Reset_completed_Eldrich.png)

--

## **5️⃣ Create and secure the confidential directory**

```
sudo mkdir /Confidential
```
**Set the directory so that:**
* Owner = root
* Group = confidential
* Only root and the confidential group have access
```
sudo chown root:confidential /confidential
sudo chmod 770 /confidential
```
![Secure created directory](Screenshots/User_root_group_confidential.png)

--

## 🎓 What I Learned

✔ Linux User Management
* Adding users with adduser
* Assigning users to groups
* Managing permissions with simple commands

✔ Password & Security Policies
* Using chage to force password resets
* Basic user lifecycle management

✔ File System Permissions
* Group ownership (chown root:confidential)
* Permission modes (chmod 770)
* Applying least privilege access

✔ Ticket-Based Workflow
* Translating requirements into commands
* Executing tasks safely as root
* Verifying results

--

## 🧠 Conclusion

This project demonstrates practical skills every entry-level IT professional needs:
* User creation
* Group management
* Password policy enforcement
* Secure directory configuration
* Understanding Linux permissions




 
 
