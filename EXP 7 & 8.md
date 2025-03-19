# Experiment 7 & 8: Managing Directories, Permissions, and umask in Linux

## Objective
Create the /home/consultants directory, add write permission for the consultants group using symbolic method, restrict access for others using octal method, and change the default umask for the operator1 user to prohibit access for users outside their group, then confirm the change.

## Steps and Commands

### Step 1: Create the /home/consultants Directory
Create the directory /home/consultants with sudo for root privileges.

#### Command:
```bash
sudo mkdir /home/consultants
```
**Screenshot:**

<img width="546" alt="Screenshot 2025-03-19 at 7 22 57 PM" src="https://github.com/user-attachments/assets/6d19d7cf-6dba-4508-87e5-e5882805b3dd" />


---

### Step 2: Add Write Permission for the consultants Group
Use the symbolic method to add write permission for the consultants group.

#### Command:
```bash
sudo chmod g+w /home/consultants
```
**Screenshot:**

<img width="546" alt="Screenshot 2025-03-19 at 7 23 46 PM" src="https://github.com/user-attachments/assets/dcc27bd7-aafe-4035-a63a-f9b534639d38" />

---

### Step 3: Restrict Access for Others Using Octal Method
Forbid others from accessing the directory by setting permissions to 770 (rwxrwx---).

#### Command:
```bash
sudo chmod 770 /home/consultants
```
**Screenshot:**

<img width="546" alt="Screenshot 2025-03-19 at 7 24 24 PM" src="https://github.com/user-attachments/assets/26559af2-2e00-4db8-8352-26c53c6dd9a0" />



---

### Step 4: Verify Directory Permissions
Check the permissions of /home/consultants to confirm changes.

#### Command:
```bash
ls -ld /home/consultants
```
**Output:**
The permissions should show `drwxrwx---`, indicating read, write, and execute for owner and group, and no access for others.

**Screenshot:**

<img width="546" alt="Screenshot 2025-03-19 at 7 25 02 PM" src="https://github.com/user-attachments/assets/9e2e3aff-dde2-4595-9758-826dcb9dc4f6" />


---

### Step 5: Create Test Files and Directory
Create a test file and directory to observe the effect of umask.

#### Command:
```bash
touch testfile
mkdir testdir
```
**Screenshot:**

<img width="546" alt="Screenshot 2025-03-19 at 7 28 40 PM" src="https://github.com/user-attachments/assets/1b7c77b4-37fe-4889-886c-b721b4b520ac" />

---

### Step 6: Change the Default umask for operator1
Set the umask to 007 to prohibit all access for users not in the group, and append it to operator1’s .bashrc.

#### Command:
```bash
echo "umask 007" >> ~/.bashrc
```
**Screenshot:**

<img width="546" alt="Screenshot 2025-03-19 at 7 27 47 PM" src="https://github.com/user-attachments/assets/dcbc17e0-c21c-4359-bd66-d9ea480344c4" />


---

### Step 7: Confirm the umask Change
Source the .bashrc or log in again, then verify the umask.

#### Command:
```bash
umask
```
**Output:**
The umask should be `0007`.

**Screenshot:**

<img width="546" alt="Screenshot 2025-03-19 at 7 27 58 PM" src="https://github.com/user-attachments/assets/01086eca-c971-4c56-b072-b4c2dc3d72c8" />


---

### Step 8: Verify Permissions on Test Files
Check the permissions of the test file and directory created earlier.

#### Command:
```bash
ls -l
```
**Output:**
The permissions should reflect the new umask (e.g., `rw-rw----` for files).

**Screenshot:**

<img width="546" alt="Screenshot 2025-03-19 at 7 28 31 PM" src="https://github.com/user-attachments/assets/56d49d5b-b1b6-4c57-b253-d7518e00dd8e" />


---

### Step 9: Switch to operator1 User
Switch to the operator1 user to ensure the umask applies.

#### Command:
```bash
sudo su - operator1
```
**Screenshot:**

<img width="546" alt="Screenshot 2025-03-19 at 7 27 41 PM" src="https://github.com/user-attachments/assets/35663919-99d0-48cd-829a-a42d61dae5af" />


---

## Conclusion
This experiment demonstrated:
- Creating a directory with `mkdir`.
- Setting group write permissions with `chmod g+w`.
- Restricting access for others using `chmod 770`.
- Changing the umask to `007` for operator1 and verifying it.
- Confirming permissions on test files reflect the new umask.

The screenshots confirm the commands were executed successfully, ensuring proper directory permissions and umask settings.

