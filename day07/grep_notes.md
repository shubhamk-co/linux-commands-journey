# 🐧 Linux Notes – `grep`, `uniq`, `find`, and `sed`

---

# 🔍 `grep` Command

## 🎯 Definition

`grep` is used to **search text or patterns inside files**.

---

## 📌 Basic Syntax

```bash
grep pattern filename
```

**Example:**

```bash
grep root /etc/passwd
```

---

# ⚙️ Important `grep` Options

## 1️⃣ `-i` → Ignore Case

```bash
grep -i root /etc/passwd
```

👉 Matches `ROOT`, `Root`, `root`.

---

## 2️⃣ `-n` → Show Line Number

```bash
grep -n root /etc/passwd
```

---

## 3️⃣ `-c` → Count Matching Lines

```bash
grep -c root /etc/passwd
```

---

## 4️⃣ `-w` → Match Whole Word

```bash
grep -w manish /etc/passwd
```

👉 Prevents partial matching.

---

## 5️⃣ `-v` → Invert Match

```bash
grep -v root /etc/passwd
```

👉 Shows lines **not containing** `root`.

---

## 6️⃣ `-o` → Show Only Matching Word

```bash
grep -o root /etc/passwd
```

---

# 📍 Context Options

## ➤ `-A` → After Lines

```bash
grep -n -A2 manish /etc/passwd
```

👉 Shows 2 lines after the match.

---

## ➤ `-B` → Before Lines

```bash
grep -n -B2 manish /etc/passwd
```

👉 Shows 2 lines before the match.

---

## ➤ `-C` → Before and After

```bash
grep -n -C3 testuser /etc/passwd
```

👉 Shows 3 lines before and after the match.

---

# 🧠 Special Characters in `grep`

## ➤ `^` → Start of Line

```bash
grep "^root" /etc/passwd
```

👉 Displays lines starting with `root`.

---

## ➤ `$` → End of Line

```bash
grep "nologin$" /etc/passwd
```

👉 Displays lines ending with `nologin`.

---

# 🔗 Multiple `grep` with Pipe

```bash
grep -i "may 17" /var/log/secure | grep useradd | grep -w manish
```

👉 Filters output step by step.

---

# 🔄 Recursive Search (`-R`)

```bash
grep -R -i skel /etc/
```

👉 Searches recursively inside directories.

---

# ⚡ Extended Regular Expressions

## Using `egrep`

```bash
egrep -n 'root|ftp|games' /etc/passwd
```

---

## Using `grep -E`

```bash
grep -n -E 'root|ftp|games' /etc/passwd
```

👉 `|` means **OR**.

---

# 📊 `uniq` Command

## 🎯 Definition

`uniq` removes or counts repeated lines.

---

## Example

```bash
grep -o root /etc/passwd | uniq -c
```

👉 Counts repeated matches.

---

# 🔍 `find` Command

## 🎯 Definition

Used to search files and directories.

---

## Basic Search

```bash
find / -name crontab
```

---

## Find Hidden Files

```bash
find /etc -name ".*"
```

---

## Find Only Files

```bash
find /home -name ".*" -type f
```

---

# 🧠 `sed` Command Basics

## Print Specific Line

```bash
sed -n '3p' /etc/passwd
```

---

## Print Multiple Lines

```bash
sed -n '3p;6p;10p' /etc/passwd
```

---

## Print Last Line

```bash
sed -n '$p' /etc/passwd
```

---

# ✏️ Replace Examples

## Add `#` at Line 3

```bash
sed '3s/^/#/' /etc/crontab
```

---

## Remove `#`

```bash
sed '3s/^#//' /etc/crontab
```

---

# ⚠️ Important

```bash
sed -i
```

👉 Modifies the original file directly.

Be careful while using it on system files. ⚠️

---

# 🔥 Key Learnings

* `grep` → Search patterns
* `uniq` → Remove or count duplicates
* `find` → Locate files and directories
* `sed` → Edit and filter text
