
### 🔧✨ **Parameter Expansion Tricks**

These tricks help you **manipulate the value of a variable** in Bash.

📌 **Assume:**

```bash
name="HELLOworld"
```

---

#### 1️⃣ `${name,}` → Lowercase **first letter**

```bash
echo ${name,}
# Output: hELLOworld
```

---

#### 2️⃣ `${name,,}` → Lowercase **entire string**

```bash
echo ${name,,}
# Output: helloworld
```

---

#### 3️⃣ `${name^}` → Uppercase **first letter**

```bash
echo ${name^}
# Output: HELLOworld (no change here because first letter is already uppercase)
```

📌 **If it were:**

```bash
name="helloWorld"
echo ${name^}
# Output: HelloWorld
```

---

#### 4️⃣ `${name^^}` → Uppercase **entire string**

```bash
echo ${name^^}
# Output: HELLOWORLD
```

---

#### 5️⃣ `${#name}` → **Length** of the string

```bash
echo ${#name}
# Output: 10
```

---

## 🔢📍 **Indexing and Substring Extraction**

This helps you **extract part of a string**.

📌 **Assume:**

```bash
text="HelloWorld"
```

---

#### 1️⃣ `${text:offset:length}` → Extract substring

```bash
echo ${text:0:5}
# Output: Hello
```

📎 *Starts at index `0`, takes `5` characters.*

---

#### 2️⃣ `${text:offset}` → From offset to end

```bash
echo ${text:5}
# Output: World
```

📎 *Starts at index `5`, goes to the end.*

---

#### 3️⃣ `${text: -5:3}` → From **end**, extract substring

> ⚠️ **Note**: There is a **space after the colon** when using negative index.

```bash
echo ${text: -5:3}
# Output: Wor
```

📎 *Starts 5 characters from the end, takes 3 characters.*

---

## ✅📊 **Summary Table**

| 🔣 Syntax      | 📖 Meaning                       | 🧪 Example Output |
| -------------- | -------------------------------- | ----------------- |
| `${var,}`      | Lowercase first letter           | `hELLOworld`      |
| `${var,,}`     | Lowercase all                    | `helloworld`      |
| `${var^}`      | Uppercase first letter           | `HelloWorld`      |
| `${var^^}`     | Uppercase all                    | `HELLOWORLD`      |
| `${#var}`      | Length of string                 | `10`              |
| `${var:2:4}`   | Substring from index 2, length 4 | `lloW`            |
| `${var: -5:3}` | Substring from end, length 3     | `Wor`             |

---

### Next
