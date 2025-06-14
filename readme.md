---
# Phonebook Application in C++
### Created by: AL-AKHIR NAYAN

---

## Description

This is a simple console-based Phonebook application built using **C++** and binary file handling. It enables users to create, view, search, modify, and delete contact records. Each record includes a person's **name**, **address**, and **phone number**.

All contact information is stored persistently in a binary file (`telephone.dat`), making the data available across sessions.

---

## Features

✅ Add New Contact  
✅ Display All Contacts  
✅ Search Contact by Phone Number  
✅ Modify Existing Contact  
✅ Delete Contact  
✅ Console-based UI with Interactive Menu  

---

## Technical Details

- **Class: `telephone`**
  - Attributes: `name`, `address`, `ph_no`
  - Methods:
    - `get()` – Get user input
    - `show()` – Display contact info
    - `getph_no()` – Retrieve phone number (used as unique key)

- **File Used:** `telephone.dat`
  - Binary format
  - Contacts are saved and read using `fstream`, `ifstream`, `ofstream`

- **Key Concepts Used:**
  - Object-Oriented Programming
  - Binary File Handling
  - Console I/O (`cin`, `cout`)
  - Input manipulation (`getline`, `ignore`)
  - C++ Standard Library

---

## File Structure

```cpp
main()                // Displays the menu and handles user choices
write_telephone()     // Adds new record
display_all()         // Shows all records
display_sp()          // Searches by phone number
modify_telephone()    // Modifies a specific record
delete_telephone()    // Deletes a record
````

---

## User Interface (Menu)

```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
1. Add Telephone Record
2. Show Records
3. Search Telephone Records
4. Modify Record
5. Delete Record
6. EXIT
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
```

---

## How to Compile & Run

### Prerequisites:

* C++ Compiler (g++, clang++ or MSVC)

### Compile with g++:

```bash
g++ phonebook.cpp -o phonebook
./phonebook
```

### On Windows (MinGW):

```bash
g++ phonebook.cpp -o phonebook.exe
phonebook.exe
```

---

## Limitations

* Uses C-style strings (fixed `char[]` arrays)
* Phone number is stored as an `int` (no support for leading zeroes or special formats)
* No input validation or error handling for bad inputs

---

## Future Enhancements

* Use `std::string` for safer and more flexible input
* Store phone numbers as strings
* Add support for searching by name/address
* Improve file format (e.g., switch to text/CSV/JSON)
* Add input validation
* GUI or web-based frontend

---

## License

This project is open-source and free to use.

---

## Acknowledgment

Thanks for checking out this project! Contributions and feedback are welcome.

```


## To **run the Phonebook application** written in C++, you need a basic development environment that supports C++ compilation and execution. Here are the **software requirements**:

---

## **Software Requirements**

### 1. **Operating System**

* **Windows**, **Linux**, or **macOS**

  * The code uses standard C++ libraries, so it's OS-independent.
  * On Windows, the `conio.h` header is used, so it's best supported with tools like **Turbo C++**, **Dev-C++**, or **MinGW**.

---

### 2. **C++ Compiler**

You need a compiler that supports standard C++. Examples:

* **Windows:**

  * [MinGW (G++)](https://www.mingw-w64.org/)
  * [Microsoft Visual C++](https://visualstudio.microsoft.com/)
  * Turbo C++ (outdated but still used in some schools)
  * Code::Blocks IDE (with built-in GCC compiler)

* **Linux/macOS:**

  * G++ (GNU Compiler Collection)
  * Clang++

> Minimum C++ standard required: **C++98 or later**
> The code does not use any C++11+ features, so older compilers are also fine.

---

### 3. **Text Editor / IDE (Optional but Recommended)**

To write, edit, and compile the code:

* **Lightweight editors:**

  * Notepad++
  * Visual Studio Code

* **IDEs:**

  * Code::Blocks
  * Dev-C++
  * Visual Studio
  * CLion

---

### 4. **Command Line / Terminal**

Used to compile and run the program:

```bash
g++ phonebook.cpp -o phonebook
./phonebook
```

Or, on Windows:

```bash
g++ phonebook.cpp -o phonebook.exe
phonebook.exe
```

---

## Important Notes

* If you’re using **Linux or macOS**, you'll need to **remove `<conio.h>`** and replace `getch()` with a standard input like `cin.get()`, because `<conio.h>` is not supported on those platforms.

  You can remove or comment this line:

  ```cpp
  #include <conio.h>
  ```

  And replace any `getch();` with:

  ```cpp
  cin.ignore();
  cin.get();
  ```

---

