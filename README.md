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
