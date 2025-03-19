# Experiment 2: Exploring Man Pages and Brace Expansion in Linux

## Objective
This experiment covers:
- Viewing the gedit man page.
- Using `man -k ext4` to find ext4 tuning commands.
- Demonstrating brace expansion to generate file name sequences.

---

## Steps and Commands

### **Step 1: View the gedit Man Page**
Displays the manual page for the gedit text editor.
```bash
man gedit
```
**Screenshots** 

<img width="598" alt="Screenshot 2025-03-19 at 7 06 01 PM" src="https://github.com/user-attachments/assets/3559364d-39ba-4ce6-80d0-532f46072991" />

<img width="780" alt="Screenshot 2025-03-19 at 7 05 50 PM" src="https://github.com/user-attachments/assets/7272a5ab-f0e9-46f6-9de1-8c63eac15a87" />


### **Step 2: Find Commands to Tune ext4 File-System Parameters**
Search for ext4-related commands using:
```bash
man -k ext4
```
The command lists tools like `tune2fs` for adjusting ext4 file-system parameters.

**Screenshots** 
<img width="869" alt="Screenshot 2025-03-19 at 7 06 40 PM" src="https://github.com/user-attachments/assets/23f9de47-9ef9-4dcf-a88d-18f1dad0b774" />



### **Step 3: Demonstrate Brace Expansion**
#### **Command 1: Generate Files with a List**
Creates files `file_A.txt`, `file_B.txt`, and `file_C.txt`.
```bash
echo file_{A,B,C}.txt
```
#### **Command 2: Generate Files with a Sequence**
Creates files `num_1`, `num_2`, and `num_3`.
```bash
echo num_{1,2,3}
```
#### **Command 3: Generate Files with a Year Sequence**
Creates `backup_2024_v1.zip` to `backup_2026_v3.zip`.
```bash
echo backup_{2024..2026}_v{1..3}.zip
```

**Screenshots** 

<img width="727" alt="Screenshot 2025-03-19 at 7 08 39 PM" src="https://github.com/user-attachments/assets/9b19ac1d-9243-4702-9a31-d9cec7ab0ec2" />


---

## Conclusion
This experiment demonstrated:
- Viewing the gedit man page with `man gedit`.
- Using `man -k ext4` to find `tune2fs` for ext4 tuning.
- Applying brace expansion to generate structured file names.

Screenshots confirm successful command execution, showcasing the power of brace expansion for automating file naming.

---
**End of Experiment**

