# advanced-linux-commands# 🖥️ Step-by-Step Linux Server Administration Tutorial 🐧

Learn how to perform essential Linux server administration tasks with this comprehensive guide! 🔧

---

## 📋 Prerequisites:
- MobaXterm installed on your local machine  
- SSH key for server authentication  
- Ubuntu server access  

---

## 🚀 Step 1: Launch MobaXterm
![Step 1 — Launch MobaXterm](Step1%20MobaXterm%20ready.png)  
Open MobaXterm on your local machine. You'll see the interface with various options like Sessions, Tools, Games, and more. This is your starting point for server connections.

---

## 🔑 Step 2: Connect to Server Using SSH Key
![Step 2 — Connect to Server](Step2%20connecting%20to%20the%20server%20with%20ssh%20key.png)  
Establish an SSH connection to your server using your private key. Once connected, you'll see the server welcome message and system information, confirming a successful connection.

---

## 📄 Step 3: Create a File and Check Permissions
![Step 3 — File Created](Step3%20File%20created%20and%20file%20permissions%20checked.png)  

Create a new script file using:  
```bash
touch script.sh
```  

Check its permissions:  
```bash
ls -lair script.sh
```  
The output shows the default permissions: `-rw-rw-r--`.

---

## ⚙️ Step 4: Add Execute Permissions
![Step 4 — Add Execute Permissions](Step4%20Files%20modified%20to%20give%20execute%20permissions.png)  

Make the script executable:  
```bash
chmod +x script.sh
```  

Verify new permissions:  
```bash
ls -lair script.sh
```  
The permissions should now be: `-rwxrwxr-x`.

---

## 🔢 Step 5: Change Permissions Using Numeric Values
![Step 5 — Numeric Permissions](Step5%20changing%20permissions%20with%20number%20values.png)  

Set specific permissions:  
```bash
chmod 755 script.sh
```  

Verify:  
```bash
ls -latt script.sh
```  
Permissions should now be: `-rwxr-xr-x`.

---

## 🌐 Step 6: Set Full Permissions for All Users
![Step 6 — Full Permissions](Step6%20Change%20permissions%20to%20allow%20group%20members%20and%20others%20to%20read%20,write%20and%20execute.png)  

Create and set full permissions:  
```bash
touch note.txt
chmod 777 note.txt
ls -lair note.txt
```  
Permissions should be: `-rwxrwxrwx`.

---

## 👑 Step 7: Switch to Superuser and Exit
![Step 7 — Superuser](Step7%20switching%20to%20a%20superuser%20with%20the%20sudo%20command%20and%20exiting.png)  

Become root:  
```bash
sudo -i
```  
Exit:  
```bash
exit
```

---

## 👤 Step 8: Create a New User
![Step 8 — New User](Step8%20user%20stiv%20created.png)  

Add a new user:  
```bash
sudo adduser stiv
```  
Follow prompts to set password and user info.

---

## 🔄 Step 9: Add User to Sudo Group and Change Password
![Step 9 — Add to Sudo](Step9%20changed%20to%20user%20stiv%20and%20password%20changed.png)  

```bash
sudo usermod -aG sudo stiv
su stiv
sudo passwd stiv
```  

---

## ✅ Step 10: Verify User Login
![Step 10 — Verify User](Step10%20password%20okay.png)  

Switch to new user:  
```bash
su stiv
```  

---

## 👥 Step 11: Create Group and Add User
![Step 11 — Group Management](step11%20user%20stiv%20added%20to%20developers%20group.png)  

```bash
sudo groupadd developers
sudo usermod -aG developers stiv
id stiv
```  
Verify user groups.

---

## 🗑️ Step 12: Delete a User
![Step 12 — Delete User](step12%20deleting%20user.png)  

Delete a user:  
```bash
sudo userdel obj
```  

---

## 💡 Summary:
- Always use `sudo` for administrative commands  
- Understand file permissions before changing them  
- Use groups to manage permissions efficiently  
- Regularly audit user accounts on your system  

---

🎉 **Nice job !**
