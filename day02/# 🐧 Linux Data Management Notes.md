# 🐧 Linux Data Management Notes

---

## 📂 Types of Paths

### 1️⃣ Relative Path

**Definition:**
A relative path specifies the location of a file or directory **with respect to the current working directory**.

**Example:**

```bash
cd documents/project
```

---

### 2️⃣ Absolute Path

**Definition:**
An absolute path specifies the complete location of a file or directory **starting from the root `/`**.

**Example:**

```bash
cd /home/user/documents/project
```

---

## 📄 `touch` Command

**Definition:**
Used to **create a new empty file**.

```bash
touch filename
```

### Create Multiple Files

```bash
touch b{1..5}
```

👉 Creates:

```
b1  b2  b3  b4  b5
```

---

## 📁 `mkdir` Command (Make Directory)

**Definition:**
Used to **create a new directory**.

```bash
mkdir data1
```

### Create Nested Directories

```bash
mkdir -p dir1/dir2/dir3
```

👉 `-p` creates parent directories automatically

---

## ⚡ Run Multiple Commands

```bash
command1 ; command2
```

👉 Runs both commands

```bash
command1 && command2
```

👉 Runs second command only if first is successful

```bash
command1 || command2
```

👉 Runs second command only if first fails

---

## 🌳 `tree` Command

**Definition:**
Displays directory structure in a **tree-like format**.

```bash
tree [directory]
```

### Useful Options

* `tree -a` → show hidden files
* `tree -L 2` → limit depth

---

## 📂 `cd` Command (Change Directory)

**Definition:**
Used to **change the current working directory**.

```bash
cd folder_name   # enter directory
cd               # go to home directory
cd ..            # move one level up
cd .             # stay in current directory
cd ../..         # move two levels up
cd -             # go to previous directory
```

---

## 📄 `cp` Command (Copy)

**Definition:**
Used to **copy files and directories**.

```bash
cp file1 file2              # copy file
cp file.txt /path/          # copy to another directory
cp -r folder1 folder2       # copy directory
```

---

## 🌲 View Directory Structure

```bash
tree
```

OR

```bash
ls -R
```

---

## ⚙️ Types of Command Options

### 🔹 Character Option (Short)

```bash
ls -l
```

### 🔹 Word Option (Long)

```bash
ls --help
```

### 🔹 Multiple Options

```bash
ls -la
```

---

## ✅ Quick Summary

* `touch` → create file
* `mkdir` → create directory
* `cd` → navigate directories
* `cp` → copy files/folders
* `tree` → show structure
* Paths → relative & absolute
* Multiple commands → `; && ||`
* Options → short, long, combined

---
