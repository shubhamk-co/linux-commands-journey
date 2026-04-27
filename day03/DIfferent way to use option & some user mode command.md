\# 🐧 Linux Practice - Day Progress Notes



\## 📅 Day: User Management \& File Operations



\---



\# 👤 User Management Commands



\## ➤ Create User



```bash

useradd rohit

```



\## ➤ Verify User Home Directory



```bash

ls /home

```



\---



\## ➤ Delete User



```bash

userdel rohit

```



👉 Observation:



\* User is deleted but \*\*home directory remains\*\*



\---



\## ➤ Delete User with Home Directory



```bash

userdel -r rohit

```



👉 `-r` removes:



\* Home directory

\* Mail spool



\---



\## ➤ Force Delete User



```bash

userdel -r -f suraj

```



👉 `-f` is used when:



\* User is logged in

\* Files still exist



\---



\## ⚠️ Important Learning



\* `userdel` without `-r` → does NOT delete home directory

\* Recreating user gives warning if home exists



\---



1️⃣ Short Options (Single Dash -)



👉 Multiple options can be combined together



userdel -r -f suraj



OR



userdel -rf suraj



👉 Both commands work the same ✔️



2️⃣ Long Options (Double Dash --)

userdel --remove --force suraj



👉 Long options are more readable but longer to type



🧠 Key Learning

\-Options can be combined in short form → -rf

\-Or written separately → -r -f

\-Long options use -- → --remove --force

\-Always check command support using:

\-command --help



\# 🏠 Custom Home Directory



\## ➤ Create Custom Directory



```bash

mkdir /testuser

```



\## ➤ Create User with Custom Home



```bash

useradd -d /testuser/user1 user1

```



\---



\# 🔧 User Modification (`usermod`)



\## ➤ Lock User



```bash

usermod -L shubham

```



\## ➤ Unlock User



```bash

usermod -U shubham

```



\## ➤ Set Expiry Date



```bash

usermod -e 2027-02-25 shubham

```



\## ➤ Add Comment



```bash

usermod -c "HR Manager" shubham

```



\---



\# 🌐 Network Command



Note:

I have not studied this command in detail yet; it is included only as an example to understand how to pronounce the option -tunlp in case it is asked during a viva.



\## ➤ Check Open Ports



```bash

netstat -tunlp

```



\# 📁 Directory \& File Operations



\## ➤ Create Directory with Permission



```bash

mkdir --mode=777 /testfile

```

\-mode=777   (it is different way to use option value )(study later)

\---



\## ➤ Create Directory with Space in Name



```bash

mkdir "shubh kumar"

mkdir 'old movie'

mkdir kartik/ singh

```



\---



