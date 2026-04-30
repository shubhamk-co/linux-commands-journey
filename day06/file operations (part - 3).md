## 📥 Output Redirection (`>` and `>>`)

### 1️⃣ `>` (Greater Than)

**Definition:**
Used to **store output into a file (overwrite mode)**.

```bash
lsblk | head -n 3 > abc/myfile
```

👉 Result:

* Output is saved in `abc/myfile`
* If file exists → **old data is deleted**

---

### 2️⃣ `>>` (Double Greater Than)

**Definition:**
Used to **append output to a file (add data at end)**.

```bash
lscpu | tail -n 3 >> abc/myfile
```

👉 Result:

* New data is added below existing content
* Old data is NOT removed

---

## 🧠 Key Difference

| Symbol | Action         |
| ------ | -------------- |
| `>`    | Overwrite file |
| `>>`   | Append to file |

---
## ❌ `rm -f` Command

**Definition:**
Used to **force delete files without confirmation**.

```bash
rm -f abc/myfile
```

## 🔁 `tee` Command

**Definition:**
The `tee` command is used to **display output on terminal AND save it into a file**.

---

### 📌 Example

```bash
lsblk | head -n 3 | tee abc/test-1
```

👉 Output:

* Displayed on screen
* Saved in file

---

### ➕ Append Mode

```bash
lscpu | head -n 3 | tee -a abc/test-1
```

👉 `-a` = append (same as `>>`)

---

## 🧠 `sed` Command (Stream Editor)

**Definition:**
`sed` is used to **filter, modify, and display specific lines from text**.

---

### 📌 Print Specific Line

```bash
sed -n '3p' /etc/passwd
```

👉 Shows only 3rd line

---

### 📌 Multiple Lines

```bash
sed -n '3p;6p;10p' /etc/passwd
```

---

### 📌 Last Line

```bash
sed -n '$p' /etc/passwd
```

---

# `script` Command (Terminal Recording)

## 🎯 Definition

The `script` command is used to **record everything that happens in the terminal session** and save it into a file.

👉 It is useful for:

* Recording practical work 🎥
* Saving command output 📄
* Creating logs for learning

---

## 💻 Syntax

```bash
script filename
```

---

## 📌 Example

```bash
script mysession.txt
```

👉 Now:

* All commands + output will be recorded

---

## ▶️ Stop Recording

Press:

```bash
exit
```

OR

```bash
Ctrl + D
```

---

## 📄 View Recorded File

```bash
cat mysession.txt
```

---

## 🔧 Append Mode

```bash
script -a mysession.txt
```

👉 `-a` → append (add new data without deleting old)

---

## 🧠 Important Points

* Records **everything on terminal**
* Useful for assignments & proof of work
* File includes:

  * Commands
  * Output
  * timestamps

---










