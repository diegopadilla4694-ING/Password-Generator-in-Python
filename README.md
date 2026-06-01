# Password-Generator-in-Python

A modern, lightweight, and secure desktop application designed in Python to instantly generate high-entropy passwords. Its graphical interface allows you to create strong credentials with a single click, automating the copying process to improve security and the user experience.

---

## Project Purpose

The main objective of this mini-software is to mitigate the use of weak or reused passwords. The application solves this problem by offering a utility tool that generates random alphanumeric strings that meet modern cybersecurity standards.

### Key Features:
* **Cryptographic Security:** It uses Python's `secrets` module, which accesses the operating system's randomness sources, ensuring that passwords are immune to probabilistic reverse engineering.

* **Forced Complexity:** The algorithm guarantees the mandatory inclusion of at least one letter, one number, and one special character (`!@#$%^&*()-_=+`).
* **Persistent Window (`Topmost`):** The interface always remains in the foreground, above other windows, ideal for interacting with it while registering on a website.

* **Anti-Edit Control:** The text field is locked as "Read Only" to prevent the user from accidentally altering the generated password.

# Modules used.

`Import`-> `customtkinter`, `secrets`, `string` `pyperclip`

Each import was used to generate a random and secure string.

**customtkinter**: Generates a more polished and visually appealing interface.

**secrets**: Generates strings or variables in a more secure and robust way.

**string**: Used to randomly convert digits and ASCII letters.

**pyperclip**: Allows me to automatically copy the password to the user's clipboard.

# Code Structure

**class password_suggestion(ctk.CTk):**
-> Contains constructors to create the graphical interface, including `self` -> title, geometry, attributes, label, configure, button, and pack.

- Main Structure:

**class password_suggestion(ctk.CTk)**
The application is encapsulated in a class that inherits from ctk.CTk to manage the main window and its states during user interaction.

**__init__(self) (Constructor):** Initializes the configured graphical interface, applying its essential properties such as the title, geometry dimensions, foreground persistence (attributes("-topmost", True)), and the distribution of components on the screen using the pack() method.


**self.password = self.secret_password():** Initializes the software or application by calling the internal function `secret_password`, which handles the algorithmic logic for generating the initial password.

**self.entry.insert(0, self.password):** Dynamically inserts the generated string into the interface's text field, which will be 12 characters long.

**self.entry.configure(state="readonly"):** Locks the text field in "Read Only" mode. This allows the user to view and select the password, but prevents accidental modifications or deletions from the keyboard.

# Interaction and Buttons
- "``Use password`" Button ```python
self.btn = ctk.CTkButton(self, text="Use password", command=self.copy_and_close)
self.btn.pack(pady=10) ```

-> This code snippet links the button to the `copy_and_close` function, which permanently copies the suggested password to the password manager and then to the user's clipboard, securely closing (destroying) the application window.

- "Change Password" Button ```python
self.btn_generar = ctk.CTkButton(self, text="Change password", command=self.generated_password)
self.btn_generar.pack(pady=10) ```

-> Invokes the `generated_password` method within the code, which temporarily alters the state of the text field within the interface to clear it, then calculates a new random password and inserts it into the user interface screen.

---

## Requirements and Installation

To run this project, you need to have **Python 3.7+** installed and the necessary external dependencies for the interface and clipboard.

Installation command:

```bash
pip install customtkinter pyperclip

## What did I learn with this project?

* **Cryptographic Security:** I learned to implement Python's `secrets` module instead of `random`, ensuring that randomness depends directly on the operating system and is suitable for strong passwords.

* **Modern GUI Development:** I experimented with `customtkinter`, learning to manage clean layouts using `pack()`, dynamic window configurations (such as `-topmost` mode), and state control for input elements (`readonly` vs. `normal`).

* **UX Optimization:** I understood how to automate system processes using