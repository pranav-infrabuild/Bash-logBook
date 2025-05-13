### Variables and Shells Expansions



---

## ✨ **Parameters in Shell Script**

🔹 In shell scripting, **parameters** are special variables that are used to pass information to and from scripts and functions.
🔹 They can be used to control the behavior of a script or function, making it more flexible and reusable. 


---

### 🔷 Types of Parameters

#### 1️⃣ Positional Parameters

* These are parameters passed to a script or function and accessed using numbers.
* Example: `$1`, `$2`, etc., represent the first, second, and subsequent positional parameters.

#### 2️⃣ Special Parameters

* These include special variables that hold specific information:

  * `$#` → Number of positional parameters
  * `$*` → All positional parameters as a single word
  * `$@` → All positional parameters as separate words
  * `$?` → Exit status of the last command

#### 3️⃣ Named Parameters / Variables

* Variables that you define within your script.
* Example:

  ```bash
  name="John"
  ```

  Assigns the value `"John"` to the variable `name`.

#### 4️⃣ Default Parameters

* You can set default values using the syntax:

  ```bash
  ${parameter:-default}
  ```
* If `parameter` is not set or is null, `default` will be used.

#### 5️⃣ Environment Variables

* Affect the behavior of the shell and other programs.
* Common examples:

  * `PATH`
  * `HOME`
  * `USER`

---



## 🔹 **1. Positional Parameters**

<details>  
<summary>📘 Click to Expand</summary>  

📌 **Positional parameters** are a way to pass arguments to a script or function.
They are accessed using numbers like `$1`, `$2`, etc.

### 🛠️ How to Use Positional Parameters

1. **Passing Arguments**

```bash
./myscript.sh arg1 arg2 arg3
```

• `arg1` is `$1`
• `arg2` is `$2`
• `arg3` is `$3`

2. **Accessing Arguments**

```bash
#!/bin/bash
echo "First argument: $1"
echo "Second argument: $2"
echo "Third argument: $3"
```

### 💡 Practical Use Cases

✅ **Automation** — for tasks like backups, deployments
✅ **Functions** — handle multiple inputs

### 📝 Tips

• ✅ **Validation**: Check the number of arguments
• ✅ **Quoting**: Use quotes to handle spaces
• 🔄 **Shift Command**: Use `shift` to manipulate parameters in loops

</details>  

---

## 🔹 **2. Special Parameters**

<details>  
<summary>📘 Click to Expand</summary>  

### 🧩 Special Parameters

* `$0` ➤ The name of the script itself
* `$#` ➤ Number of arguments passed
* `$@` ➤ All arguments (separate words)
* `$*` ➤ All arguments (single word)
* `$$` ➤ Process ID of the script
* `$?` ➤ Exit status of the last command

### 🔍 Example Script

```bash
#!/bin/bash
echo "Script name: $0"
echo "Number of arguments: $#"
echo "All arguments: $@"
echo "First argument: $1"
echo "Second argument: $2"
```

</details>  

---

## 🔹 **3. Named Parameters / Variables**

<details>  
<summary>📘 Click to Expand</summary>  

### ✍️ 1. **Defining Variables**

📌 **Syntax**: No spaces around `=`

```sh
name="John"
age=30
```

### 👓 2. **Accessing Variables**

📌 Use `$` before variable name

```sh
echo $name
echo $age
```

### 🧷 3. **Quoting Variables**

• **Double Quotes** — preserve spaces

```sh
greeting="Hello, $name"
echo "$greeting"
```

• **Single Quotes** — treat literally

```sh
greeting='Hello, $name'
echo "$greeting"  # Outputs: Hello, $name
```

</details>  

---

## 🔹 **4. Default Parameters**

<details>  
<summary>📘 Click to Expand</summary>  

### 🧰 What Are Default Parameters?

🔸 They ensure your script has a fallback value.
🔸 Useful for making scripts more user-friendly and robust.

### 📐 Syntax

```bash
${parameter:-default}
```

### 🔄 How It Works

• If `parameter` is set → return its value
• If not set/null → return `default`

### 📋 Example

```bash
#!/bin/bash
name=${1:-"Guest"}
echo "Hello, $name!"
```

### ▶️ Output

• Run `./myscript.sh Alice` ➝ `Hello, Alice!`
• Run `./myscript.sh` ➝ `Hello, Guest!`

</details>  

---

---
[Jump to Next Topic ](#variables-and-shells-expansions)



