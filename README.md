### Command: whoami
- **Purpose:** Check current logged-in user
- **Output:** ubuntu
- **Takeaway:** I confirmed I’m logged in with the default Ubuntu user account.
<img width="1929" height="907" alt="whoami" src="https://github.com/user-attachments/assets/ec65af73-84af-49ce-a2ff-d60ef14db66b" />



### Command: pwd
- **Purpose:** Print working directory (where I am in the file system).
- **Output:** /home/ubuntu
- **Takeaway:** Validated my current directory.
<img width="1944" height="897" alt="PWD " src="https://github.com/user-attachments/assets/bcc06a09-2f3b-4b7b-bc61-6161af560edc" />

### Command: ls -l
- **Purpose:** List files and directories with details (permissions, owner, size, date).
- **Output:** Shows items in `/home/ubuntu` with their permission settings.
- **Takeaway:** Learned how Linux controls access with `rwx` permissions.
- **Expected Output:** A detailed list showing file permissions, owners, sizes, etc.
- **Actual Output:** I typed the wrong flag at first and got `command not found`.
- **Takeaway:** Learned that Linux commands are case-sensitive and require exact syntax.
<img width="1972" height="903" alt="-I" src="https://github.com/user-attachments/assets/2780c8c5-3b70-4bbb-819f-288233a515f7" />


### Command: uname -a
- **Purpose:** Display system/kernel information.
- **Output:** Linux ip-172-31-xx-xx ... Ubuntu 24.04 ... x86_64 GNU/Linux
- **Takeaway:** Confirmed I’m running Ubuntu 24.04 with the Linux kernel.
<img width="1928" height="918" alt="uname -a" src="https://github.com/user-attachments/assets/0ca6dde2-68bc-470e-a87b-71f796117f50" />


### Command: df -h
- **Purpose:** Show disk usage in human-readable format.
- **Output:** Displays root filesystem size and free space.
- **Takeaway:** Learned how to monitor server storage to avoid running out of space.
<img width="1943" height="927" alt="df -h" src="https://github.com/user-attachments/assets/89f833dc-fbd3-4c95-95bd-56efcea92e20" />


### Command: free -m
- **Purpose:** Check memory usage in MB.
- **Output:** Shows “Mem” and “Swap” values.
- **Takeaway:** Verified how much RAM is available on the server.
<img width="1936" height="921" alt="free -m" src="https://github.com/user-attachments/assets/d654aa5f-138a-4a76-ba3b-baf2b852133c" />


### Command: uptime
- **Purpose:** Check system uptime, users logged in, and load averages.
- **Output:** 09:23:12 up 12 min, 1 user, load average: 0.00, 0.01, 0.05
- **Takeaway:** Learned how to do a quick health check of the system’s stability.
  <img width="1923" height="923" alt="uptime" src="https://github.com/user-attachments/assets/2012ac76-fea1-49f3-8e97-f0300494cafe" />



## Lab 2: Linux Security Hardening

### Command: adduser
- **Purpose:** Create a new user account.
- **Output:** Prompted for password and user details.
- **Takeaway:** Ensured I don’t rely only on the default `ubuntu` user.
  <img width="1936" height="926" alt="Add Group" src="https://github.com/user-attachments/assets/2a84bee8-fd3d-46ce-b504-b8f9340b30db" />



  ### Command: usermod -aG sudo calvin
- **Purpose:** Add new user to sudo group.
- **Output:** (No output)
- **Takeaway:** Granted my new user administrative privileges.
<img width="1951" height="902" alt="adduser sudo Calvin" src="https://github.com/user-attachments/assets/c41ad8fb-add6-4605-a796-e67203608075" />


### Command 1: `sudo ufw enable`
- **Purpose:** Enable UFW firewall.
- **Output:** Warning appeared: "Command may disrupt existing SSH connections. Proceed with operation (y|n)?"
- **Action:** Typed `y` to confirm since I had already allowed SSH (port 22).
- **Takeaway:** Learned that enabling UFW without allowing SSH first can lock you out. This is a key step in Linux server hardening.
  <img width="1941" height="970" alt="sudo ufw enable " src="https://github.com/user-attachments/assets/e1220982-2cc5-43dd-a476-d239d36d2d87" />

  **Command 2: `sudo ufw allow 22/tcp`**
- **Purpose:** Explicitly allows inbound SSH traffic on port 22 (TCP).
- **Output:** Confirmation message showing the rule was added.
- **Takeaway:** Ensured I can still access the server securely via SSH even with the firewall enabled.
<img width="1943" height="932" alt="sudo ufw allow 22 cup" src="https://github.com/user-attachments/assets/ab42a44e-535e-434f-85d0-56201bb1e78d" />

**Command 3: `sudo ufw status`**
- **Purpose:** Verify firewall status and active rules.
- **Output:** Shows `Status: active` with rules like:
<img width="1933" height="947" alt="sudo ufw status " src="https://github.com/user-attachments/assets/74a9193b-0b8d-4c1c-ac6f-2cf7388f8e80" />


 ### Fail2Ban – Brute-force Protection

**Command 1: `sudo apt update && sudo apt install fail2ban -y`**
- **Purpose:** Updates package list and installs Fail2Ban.
- **Output:** Installation messages confirming the package was downloaded and installed.
- **Takeaway:** Installed Fail2Ban on Ubuntu to protect against repeated failed login attempts.


**Command 2: `sudo systemctl enable --now fail2ban`**
- **Purpose:** Starts Fail2Ban immediately and enables it to run on every boot.
- **Output:** No output on success, but Fail2Ban is now active in the background.
- **Takeaway:** Ensured that brute-force protection is always running without needing manual start.sudo system

**Command 3: `systemctl status fail2ban`**
- **Purpose:** Check that the Fail2Ban service is running.
- **Expected Output:**

  <img width="1939" height="975" alt="Brute force 1 " src="https://github.com/user-attachments/assets/6ffd308c-5c16-4ae0-b03c-79315db2e282" />
  <img width="1912" height="911" alt="Bruce force 2 " src="https://github.com/user-attachments/assets/d93a7222-0f29-4443-b383-391cb20899c9" />


