🌍 DISTANCE BETWEEN TWO POINTS CALCULATOR 🌍
===========================================

This compiler calculates the Euclidean distance between two 2D points using:

📏 distance = sqrt((x2-x1)² + (y2-y1)²)

✨ OUTPUTS GENERATED:
✅ Three Address Code (TAC)
⚡ Optimized Assembly Instructions
💻 Register-based Machine Code

📥 INSTALLATION
--------------
🔧 1. Install MSYS2 from https://www.msys2.org/

🔧 2. Run these commands in MSYS2 terminal:

   pacman -Su
   pacman -S base-devel gcc flex bison
   pacman -S git cmake (optional)

🔨 BUILD INSTRUCTIONS
------------------
1. make
2. Executable 'distance_calculator' will be created

🚀 USAGE EXAMPLE
-------------
📝 Input format:
DISTANCE = POINT(3, 4) TO POINT(6, 8);

📊 Sample Output:

💠 Three Address Code:

t1 = 6 - 3

t2 = t1 * t1

t3 = 8 - 4

t4 = t3 * t3

t5 = t2 + t4

t6 = sqrt(t5)

DISTANCE = t6

⚡ Optimized Assembly:

MOV R1, 6

SUB R1, R1, 3

MUL R1, R1, R1

MOV R2, 8

SUB R2, R2, 4

MUL R2, R2, R2

ADD R3, R1, R2

SQRT R4, R3

STORE DISTANCE, R4

🎯 OPTIMIZATIONS
-------------

🔍 Patterns optimized:

- (a-b)*(a-b) → SUB_SQUARE

- a²+b² → ADD_SQUARES
  

📂 FILES
-----

📄 lexer.l    - Flex lexer definitions

📄 parser.y   - Bison parser rules

📄 main.cpp   - Main program

📄 Makefile   - Build configuration


📜 LICENSE
-------
MIT License - Free to use and modify
