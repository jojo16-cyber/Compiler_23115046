🧮 Distance Calculator Compiler

This project is a simple compiler built using Flex and Bison in C++. It takes an arithmetic expression that defines two coordinate points and calculates the Euclidean distance between them.

It generates:

✅ Three Address Code (TAC)
⚙️ Optimized Custom Instructions (like DIST_SQR, SQRT)
🖥️ Register-based Assembly Output

Built to simulate a basic register machine and demonstrate compiler design with pattern optimization.


📥 Installation Guide (Windows with MSYS2)

🔧 Step 1: Install MSYS2 Terminal
👉 Download & install MSYS2 from the official site:
🔗 https://www.msys2.org/wiki/MSYS2-installation/
Follow all initialization steps!

🛠️ Step 2: Open MSYS2 Terminal and Run These Commands
bash
Copy
Edit
pacman -Su                   # Update all packages  
pacman -S base-devel gcc     # Install base tools and C++ compiler  
pacman -S flex bison         # Install Flex & Bison  
pacman -S git                # (Optional) Version control  
pacman -S cmake              # (Optional) Build tools  
🛠 Build Instructions
Ensure flex, bison, and g++ are installed.

bash
Copy
Edit
make
This will:

Generate the parser and lexer files

Compile all source code

Create an executable called distancecalc


🚀 How to Use
Run the program:

bash
Copy
Edit
./distancecalc
You will be prompted to enter a distance expression like:

ini
Copy
Edit
DIST = distance((X1, Y1), (X2, Y2));
✅ Example Output
Section	Output
Input	DIST = distance((X1, Y1), (X2, Y2));
Three Address Code	
ini
Copy
Edit
t1 = X2 - X1  
t2 = t1 * t1  
t3 = Y2 - Y1  
t4 = t3 * t3  
t5 = t2 + t4  
DIST = sqrt(t5)
| Optimized Instructions |

java
Copy
Edit
DIST_SQR R5 = (X2 - X1)^2 + (Y2 - Y1)^2  
SQRT R6 = sqrt(R5)
| Assembly Code |

vbnet
Copy
Edit
MOV R1, X1  
MOV R2, X2  
SUB R3, R2, R1  
MUL R4, R3, R3  
MOV R5, Y1  
MOV R6, Y2  
SUB R7, R6, R5  
MUL R8, R7, R7  
ADD R9, R4, R8  
SQRT R10, R9  
STORE DIST, R10
Assembly is also saved to output.asm.


📁 Project Structure

bash
Copy
Edit
.
├── lexer.l         # Lexer (Flex)  
├── parser.y        # Parser + Code Gen (Bison)  
├── main.cpp        # Entry point  
├── Makefile        # Build script  
├── output.asm      # Assembly output  
└── README.md       # You're here!
⚙️ Optimization Details
Pattern	Recognized As
(X2 - X1)^2 + (Y2 - Y1)^2	DIST_SQR
sqrt(...)	SQRT
These patterns are recognized during parsing and mapped to custom pseudo-instructions.


📸 Screenshots
Add screenshots of terminal usage and output here
##Output

![WhatsApp Image 2025-04-06 at 16 47 50](https://github.com/user-attachments/assets/8b5761ef-f29b-44d1-b7ac-a868dbd5f343)
![WhatsApp Image 2025-04-06 at 16 47 51](https://github.com/user-attachments/assets/43c7f809-a8e9-4583-8aee-40247763d099)
![WhatsApp Image 2025-04-06 at 16 47 51 (1)](https://github.com/user-attachments/assets/39a5e7d4-ec6a-4b77-92a7-ccfd3ea07865)



📜 License
MIT License – feel free to use, modify, and enhance.

Let me know if you'd like the parser.y, lexer.l, or any source files structured too!
