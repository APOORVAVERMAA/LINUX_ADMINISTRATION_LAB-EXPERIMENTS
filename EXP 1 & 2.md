# Experiment 1: Creating Files and Directories in Linux

## Objective
This experiment demonstrates how to:
- Create multiple directories using `mkdir`.
- Create sets of empty files using `touch`.
- Organize files into directories efficiently.
- List files using `ls`.

---

## Steps and Commands

### **Step 1: Navigate to the Desktop**
Change the working directory to `Desktop`:
```bash
cd Desktop
```

### **Step 2: Create Subdirectories**
Create three subdirectories (`friends`, `family`, `work`) using a single command:
```bash
mkdir friends family work
```

### **Step 3: Create Files in Each Directory**

#### **In `friends` Directory:**
```bash
cd friends

touch song{1..6}.mp3 snap{1..6}.jpg film{1..6}.avi

ls
```

#### **In `family` Directory:**
```bash
cd ../family

touch song{1..6}.mp3 snap{1..6}.jpg film{1..6}.avi

ls
```

#### **In `work` Directory:**
```bash
cd ../work

touch song{1..6}.mp3 snap{1..6}.jpg film{1..6}.avi

ls
```

---

## Conclusion
This experiment successfully demonstrated:
- Creating directories using `mkdir`.
- Creating multiple empty files at once using `touch`.
- Using `ls` to list files and confirm their creation.

If you encounter the error:
```bash
bash: cd: friends: No such file or directory
```
This may be due to a typo or a permissions issue when creating directories. Ensure that `mkdir` executed successfully before proceeding to file creation.

---

## Screenshot
<img width="640" alt="Screenshot 2025-03-19 at 10 15 46 AM" src="https://github.com/user-attachments/assets/1dbbdd5f-fa84-4dcf-9602-b9b756e3d02a" />


---

**End of Experiment**
