# 🐧 Linux Notes – File Handling, Commands & Concepts

---

# 📄 `cat` Command

**Definition:**
The `cat` command is used to **display, create, and combine file contents** in the terminal.

### Examples

```bash id="c1"
cat file.txt
cat file1 file2
```

### Useful Options

```bash id="c2"
cat -n file.txt   # show line numbers
cat -b file.txt   # number non-empty lines
```


---

# 🔄 `tac` Command

**Definition:**
The `tac` command is used to **display file content in reverse order (last line first)**.

```bash id="t1"
tac file.txt
```

---

# 📦 Anaconda File (`anaconda-ks.cfg`)

**Definition:**
This file is generated during **OS installation** and stores:

* Installation settings
* Partition details
* Language & keyboard configuration

```bash id="a1"
cat anaconda-ks.cfg
```

---

# 📂 `ls -l` Command

**Definition:**
Displays **detailed information** about files and directories.

### File Types:

* `-` → File
* `d` → Directory
* `l` → Link (shortcut)

---

# 👁️ Hidden vs Normal Files

### Hidden Files

* Start with `.`
* Example: `.bashrc`, `.secretfile`

### View Hidden Files

```bash id="h1"
ls -a
```

---

# 🔁 Rename Hidden File

```bash id="h2"
mv .secretfile secretfile
mv secretfile .secretfile
```

---

# 🔍 `find` Command

**Definition:**
Used to **search files and directories**.

```bash id="f1"
find /etc -name ".*"
find /home -name ".*" -type f
```

---

# 📍 Special Directories

| Symbol | Meaning           |
| ------ | ----------------- |
| `.`    | Current directory |
| `..`   | Parent directory  |

---

# 📊 `ls -h` Option

**Definition:**
Displays file sizes in **human-readable format** (KB, MB, GB).

```bash id="l1"
ls -lh
```

---

# 🔗 Original File vs Shortcut (Link)

## Hard Link (Original File)

* Same inode number
* Acts as original file

## Soft Link (Shortcut)

* Points to original file
* Different inode

```bash id="ln1"
ln file1 file2       # hard link
ln -s file1 link1    # soft link
```

---

# ⚙️ Binary Types

## 1️⃣ Normal Binary

* Regular executable programs
* Example: `/usr/bin/ls`

## 2️⃣ Super Binary (SUID)

* Runs with **root privileges**
* Used for system-level operations

```bash id="b1"
ls -l /usr/bin/passwd
```

👉 Look for `s` in permissions

---

# 🔎 `which` Command

**Definition:**
Shows the **path of a command**.

```bash id="w1"
which cat
which ls
```

---

# 🔎 `whereis` Command

**Definition:**
Finds:

* Binary file
* Source file
* Manual pages

```bash id="w2"
whereis mkdir
whereis touch
```

---

# 🧠 Inode

**Definition:**
An inode is a **unique number assigned to each file** in Linux.

```bash id="i1"
ls -i file.txt
```

👉 Stores:

* File metadata
* Permissions
* Owner

---

# 🏷️ `alias` Command

**Definition:**
Used to **create shortcuts for commands**.

```bash id="al1"
alias ll='ls -l'
```

👉 Now:

```bash id="al2"
ll
```

---

