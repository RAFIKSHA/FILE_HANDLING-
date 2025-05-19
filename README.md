
---

## 📁 What is File Handling?

**File handling** in Python allows you to **create**, **read**, **write**, and **delete** files from your program.

---

## 🧰 Step-by-Step Python File Handling

---

### ✅ Step 1: Open a File

**Syntax:**

```python
file = open("filename", "mode")
```

**Modes:**

| Mode  | Description                    |
| ----- | ------------------------------ |
| `'r'` | Read (default)                 |
| `'w'` | Write (overwrites file)        |
| `'a'` | Append (adds to file)          |
| `'x'` | Create file, error if exists   |
| `'b'` | Binary mode (`rb`, `wb`, etc.) |

---

### ✅ Step 2: Read from a File

```python
file = open("demo.txt", "r")

# Read the whole file
content = file.read()
print(content)

# OR read line by line
# line = file.readline()
# lines = file.readlines()

file.close()
```

---

### ✅ Step 3: Write to a File

```python
file = open("demo.txt", "w")
file.write("Hello, world!\nThis is Python.")
file.close()
```

> Note: `'w'` will **overwrite** the file if it already exists.

---

### ✅ Step 4: Append to a File

```python
file = open("demo.txt", "a")
file.write("\nThis is an appended line.")
file.close()
```

---

### ✅ Step 5: Use `with` Statement (Best Practice)

Automatically closes the file.

```python
with open("demo.txt", "r") as file:
    content = file.read()
    print(content)
```

---

### ✅ Step 6: Check If File Exists (Optional)

```python
import os

if os.path.exists("demo.txt"):
    print("File exists")
else:
    print("File does not exist")
```

---

### ✅ Step 7: Delete a File

```python
import os

if os.path.exists("demo.txt"):
    os.remove("demo.txt")
    print("File deleted")
else:
    print("File not found")
```

---

## 🧪 Example: Read and Count Words

```python
with open("demo.txt", "r") as file:
    text = file.read()
    words = text.split()
    print("Number of words:", len(words))
```

---

## 🧠 Summary of Common Methods

| Method        | Purpose                |
| ------------- | ---------------------- |
| `read()`      | Read entire file       |
| `readline()`  | Read one line          |
| `readlines()` | Read all lines as list |
| `write(text)` | Write text to file     |
| `close()`     | Close the file         |
| `with open()` | Open with auto-close   |

---

Would you like practice exercises or a mini project involving file handling (e.g., text editor, log file reader)?
