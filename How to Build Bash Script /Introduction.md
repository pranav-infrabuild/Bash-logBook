### Introduction 

### ✅ What is Shell?
- A **shell** refers to a *command-line interface* that allows users to interact with the operating system by executing commands and scripts. 
- 💡 **Shell scripting** involves writing a series of commands in a file, known as a *script*, which can be executed by the shell to automate tasks.

---

### ✅ What is Bash?
- 🐚 A **specific type of shell** with advanced features and widespread use.
  - 📜 **Command history**: Allows users to recall and reuse previous commands.
  - ⌨️ **Tab completion**: Helps complete file names and commands by pressing the **Tab** key.
  - 🔁 **Scripting capabilities**: Supports complex scripting with **loops**, **conditionals**, **functions**, and more.
  - ⚙️ **Customization**: Users can customize their Bash environment with configuration files like `.bashrc` and `.bash_profile`.

---

### ✅ Bash Script Structure
- **Shebang Line**: The first line of a Bash script typically starts with:
  
  ```bash
  #!/bin/bash
  


#### 💡 Example of a simple Bash script:

```bash
#!/bin/bash
# This is a simple Bash script
echo "Hello, World!"
```

> 📝 The **shebang line** (`#!/bin/bash`) at the beginning of a script is a special line that tells the OS which interpreter to use.

---

### 🔍 Breakdown of the Shebang Line

1. **Shebang (`#!`)**: The characters `#!` are known as the **shebang** or **hashbang**.
2. **Interpreter Path (`/bin/bash`)**: Specifies the path to the interpreter that should execute the script.

---

### 💬 Comments in Bash

Comments in Bash scripts are ignored during execution and used for documentation.

#### ✅ Single-Line Comments:

```bash
# This is a single-line comment
echo "Hello, World!"  # This is an inline comment
```

---

### 🌟 Benefits of Using Comments

* 📖 **Clarity**: Explains what the code does.
* 🛠️ **Maintenance**: Easier to update and troubleshoot.
* 🐞 **Debugging**: Helps identify and understand logic during debugging.

---

### 🔐 Breakdown of File Permissions

#### 📄 Example Output:

```
-rwxr-xr--
```

---

### 🧩 Breakdown:

1. **File Type**:

   * `-` : Regular file
   * `d` : Directory
   * `l` : Symbolic link
   * `b` : Block device
   * `c` : Character device

2. **Owner Permissions (`rwx`)**:

   * `r` : Read
   * `w` : Write
   * `x` : Execute

3. **Group Permissions (`r-x`)**:

   * `r` : Read
   * `-` : No write permission
   * `x` : Execute

4. **Other Permissions (`r--`)**:

   * `r` : Read
   * `-` : No write
   * `-` : No execute

---

### 🔧 Example Breakdown

For `-rwxr-xr--`:

* 📂 `-`: Regular file
* 👤 `rwx`: Owner can read, write, execute
* 👥 `r-x`: Group can read and execute
* 🌐 `r--`: Others can only read

---

### 🔁 Changing File Permissions with `chmod`

Use `chmod` with **octal numbers** to set permissions.

#### 🧮 Octal Representation:

| Permission  | Value |
| ----------- | ----- |
| Read (r)    | 4     |
| Write (w)   | 2     |
| Execute (x) | 1     |

💡 Combine values:

* `7` = **Read + Write + Execute** (4+2+1)
* `6` = **Read + Write** (4+2)
* `5` = **Read + Execute** (4+1)

---

### ✍️ Example Usage:

```bash
chmod 755 filename
```

* **Owner (7)**: Read, write, execute
* **Group (5)**: Read, execute
* **Others (5)**: Read, execute

---

### ✨ Another Example:

```bash
chmod 644 filename
```

* **Owner (6)**: Read, write
* **Group (4)**: Read
* **Others (4)**: Read

---

### ✅ Applying Permissions

```bash
chmod 754 example.txt
```

* 📥 **Owner**: Read, write, execute
* 📥 **Group**: Read, execute
* 📥 **Others**: Read only

---

---

## [Solve Task 1](https://github.com/pranav-infrabuild/Bash-logBook/blob/main/How%20to%20Build%20Bash%20Script%20/Task%201.md)

