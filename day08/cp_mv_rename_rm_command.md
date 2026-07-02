# 🐧 Linux Notes – `cp`, `mv`, and `rm` Commands

---

# 📋 `cp` Command (Copy)

## 🎯 Definition

The `cp` command is used to **copy files and directories** from one location to another **within the same machine**.

### 📌 Syntax

```bash
cp SOURCE DESTINATION
```

**Example:**

```bash
cp vipin /data
```

---

# 📂 Copy Directory

Use the **`-r` (recursive)** option to copy directories.

```bash
cp -r green data-1
```

---

# ⚙️ Common Options

| Option | Description                                              |
| ------ | -------------------------------------------------------- |
| `-r`   | Copy directories recursively                             |
| `-f`   | Force overwrite without confirmation                     |
| `-i`   | Ask before overwriting existing files                    |
| `-v`   | Display each copied file (verbose)                       |
| `-p`   | Preserve original permissions, ownership, and timestamps |

**Example:**

```bash
cp -rf /data/* dircopy
```

---

# 📌 Copy Selected Files Using Wildcards

### Copy all Python files

```bash
cp *.py python
```

---

### Copy files starting with `he`

```bash
cp he* starting_words
```

---

### Copy files ending with `.conf`

```bash
mkdir example
cp /etc/*.conf example
```

This copies only configuration files (`.conf`) from `/etc`.

---

# 📌 Rename While Copying

```bash
cp /etc/crontab data-1/mycrontab
```

A copy is created with a new name.

---

# 📌 Copy Hidden Files

```bash
cp -rf .ibm data-1
```

Hidden files (starting with `.`) can also be copied.

---

# 📌 Copy Hidden Directory

```bash
cp -rfv green data-1
```

**Output:**

```text
'green' -> 'data-1/green'
'green/.data' -> 'data-1/green/.data'
```

---

# 📌 Preserve File Metadata

```bash
cp -rp abc file-B
```

The `-p` option preserves:

* File permissions
* Ownership
* Timestamp

---

# 🚀 SCP (Secure Copy)

## 🎯 Definition

`scp` is used to **copy files between two different machines over SSH**.

### 📌 Syntax

```bash
scp file.txt username@IP:/destination/path
```

### Copy Directory

```bash
scp -r project username@IP:/home/user/
```

> **Note:** `scp` is used between different systems, while `cp` is used within the same system.

---

# ❌ `rm` Command (Remove)

## 🎯 Definition

The `rm` command is used to **delete files and directories**.

---

## Delete File

```bash
rm file.txt
```

---

## Ask Before Deleting

```bash
rm -i file.txt
```

---

## Force Delete

```bash
rm -f file.txt
```

Deletes the file without confirmation.

---

## Delete Directory

```bash
rm -r directory
```

---

## Force Delete Directory

```bash
rm -rf directory
```

---

## Verbose Delete

```bash
rm -rfv directory
```

Displays every deleted file.

---

## Delete Using Wildcards

### Delete all Python files

```bash
rm -rf *.py
```

### Delete all Shell scripts

```bash
rm -rf *.sh
```

### Delete all files beginning with `google`

```bash
rm -rfv google*
```

---

## `rmdir` vs `rm -r`

### `rmdir`

Deletes **only empty directories**.

```bash
rmdir data-1
```

---

### `rm -r`

Deletes directories even if they contain files.

```bash
rm -rf data-1
```

---

# 🚚 `mv` Command (Move)

## 🎯 Definition

The `mv` command is used to **move or rename files and directories**.

---

## Move File

```bash
mv xyz /linux
```

---

## Move Directory

```bash
mv green notebook /fidora
```

---

## Rename File

```bash
mv tcs ibm
```

---

## Rename Directory

```bash
mv pen logic
```

---

# 🔄 Difference Between `cp` and `mv`

| `cp`                 | `mv`                            |
| -------------------- | ------------------------------- |
| Creates a copy       | Moves the original file         |
| Original remains     | Original location becomes empty |
| Used for duplication | Used for moving or renaming     |

---

# 📚 Key Learnings

* `cp` copies files and directories.
* `cp -r` copies directories.
* `cp -p` preserves file metadata.
* Wildcards (`*`) help copy selected files.
* `scp` copies files between different machines.
* `rm` removes files.
* `rm -rf` deletes directories forcefully.
* `mv` moves and renames files/directories.
* `cp` keeps the original file, while `mv` does not.

---
