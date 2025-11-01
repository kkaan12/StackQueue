# 🧱 MyStack – Custom Stack with Middle Element Access (Java)

This project is a **custom Stack implementation in Java** using a **doubly linked list**.  
Unlike a regular stack, this version allows you to **access and delete the middle element in O(1) time**, while maintaining standard `push()` and `pop()` operations.

---

## 🚀 Features

- `push(int data)` → Adds a new element to the top of the stack.  
- `pop()` → Removes and returns the top element.  
- `deleteMiddle()` → Deletes and returns the middle element in **constant time (O(1))**.  
- `printList()` → Prints all elements and shows which node is currently the middle.

---

## ⚙️ How It Works

The stack keeps track of:
- `head` → the top node  
- `middle` → a pointer to the middle node  
- `size` → total number of elements  

Each time an element is pushed or popped, the `middle` pointer is updated:
- When **pushing**, if the new size is **odd**, `middle` moves **one step backward**.  
- When **popping**, if the new size is **even**, `middle` moves **one step forward**.  

This mechanism ensures **O(1)** access to the middle element at all times.

---

## 🧩 Classes Overview

| Class | Description |
|-------|--------------|
| **Node** | Represents a doubly linked list node (`data`, `prev`, `next`). |
| **MyStack** | Core logic for stack operations and middle element handling. |
| **Main** | Demonstrates stack operations step-by-step with console output. |

---

## 💻 Example Output

```text
--- Stack Uygulaması Başlatılıyor ---
Stack size: 0
EMPTY

--- 1. PUSH ---
Stack size: 1
10
Middle
->

Stack size: 2
20
-> 
10
Middle
->

...
--- 2. POP ---
«Deleted Node(Pop): 50

--- 3. DELETE MIDDLE ---
Deleted Middle Element: 20
