# bookstore-management-assembly
A Bookstore Management System written in x86 Assembly (MASM/TASM) for my CSE341 Final Assessment
# 📚 Bookstore Management System (x86 Assembly)

### 🧠 Overview  
This project is a **Bookstore Management System** written in **x86 Assembly language** using **MASM/TASM**.  
It simulates a simple bookstore menu where users can browse book categories, select books, and calculate the total price of their selected items.  
All user interactions happen through DOS interrupt services (`INT 21h`).

---

## 🛠️ Features  
- 🏷️ Displays a **welcome menu** and book categories  
- 📖 Allows users to choose between **English Novels**, **Bangla Novels**, and **Historic Books**  
- 💰 Each category lists books with **titles and prices**  
- 🧾 Users can **select books** by entering their corresponding number  
- 🧮 The system **calculates and displays the total price** of selected books using stack operations  
- 🚫 Handles **invalid selections** properly  
- 🖥️ Returns control to DOS after execution  

---

## ⚙️ Technical Details  
- **Language:** Assembly (MASM/TASM compatible)  
- **Processor:** 8086 microprocessor  
- **Assembler:** MASM / TASM  
- **Execution Environment:** DOSBox or any 8086 emulator  

### 🧩 Interrupts & Registers Used
- `INT 21h` → DOS input/output  
- `AH = 09h` → Display string  
- `AH = 01h` → Take character input  
- `AH = 02h` → Display single character  
- Registers used: `AX`, `BX`, `CX`, `DX` for data operations  
- Stack operations (`PUSH`, `POP`) for summing book prices  

---


💾 How to Run

Open DOSBox or your preferred 8086 emulator.

Assemble the program:

tasm bookstore.asm
tlink bookstore.obj


Run the executable:

bookstore.exe


Follow the on-screen menu to select books and view your total.




Welcome to the Bookstore!

Choose a category:
1. English Novels
2. Bangla Novels
3. Historic Books

Enter your choice: 1

1. Things Fall Apart : Fiction, $45
2. Wuthering Heights : Fiction, $30

Select book: 1
Total Price: $45
