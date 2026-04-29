## 🗣️ `echo` Command

**Definition:**
The `echo` command is used to **display text or variables on the terminal**.

---

### 📌 Examples

```bash
echo hello yoooo kya ho raha haaa
```

👉 Output:

```
hello yoooo kya ho raha haaa
```

---

```bash
echo "kuch nahi bro"
echo 'linux padh raha hu in deeply'
```

## 📊 `wc` Command (Word Count)

**Definition:**
The `wc` command is used to **count lines, words, and characters in a file**.

---

### 📌 Example

```bash
wc /etc/passwd
```

👉 Output:

```
38   81   2091
```

* 38 → lines
* 81 → words
* 2091 → characters

---

## 🔹 Options

```bash
wc -l file   # lines
wc -w file   # words
wc -c file   # characters
```

---

## 🔹 Combine Options

```bash
wc -lcw /etc/passwd
```

## ⚡ Running Multiple Commands

**Definition:**
Use `;` to run multiple commands in one line.

---

### 📌 Example

```bash
cal ; date
```

```bash
ls . ; ls /home
```

---
## 🔗 Pipe (`|`) with `head` and `tail`

**Definition:**
Pipe `|` sends output of one command to another command.

---

### 📌 Examples

```bash
cat -n /etc/crontab | head -n 2
```

👉 Shows first 2 lines

---

```bash
lscpu | cat -n | tail -n 2
```




