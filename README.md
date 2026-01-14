# 🐍 Console Snake Game

A high-performance implementation of the classic Snake game running entirely in the C# console. Unlike basic tutorials, this project uses a non-blocking game loop and custom rendering techniques to ensure smooth gameplay without screen flickering.

### 🎯 The Problem
Building a real-time game in a console environment is challenging because standard input methods pause the program (blocking execution). The goal was to create a responsive game engine that handles user input, game logic updates, and rendering simultaneously.

### 🛠 Tech Stack
* **Language:** C# (.NET Framework)
* **Core Concepts:** `System.Threading`, `Stopwatch` (High-precision timing), Event Loops
* **Interface:** Command Line / Console

### ✨ Key Features
* **Flicker-Free Rendering:** Instead of clearing the whole screen every frame (which causes flashing), the engine only updates the specific pixels that changed (the new head position and the deleted tail).
* **Non-Blocking Input:** Uses `Console.KeyAvailable` to listen for arrow keys asynchronously, ensuring the snake keeps moving even when no key is pressed.
* **Precise Timing:** Implements a `Stopwatch` based game loop to ensure consistent speed across different computers.
* **Coordinate System:** Uses a custom `pixel` struct to manage X/Y coordinates for the snake body and food generation.

### 💡 Challenges & Learnings
* **Thread Sleeping vs. Delta Time:** I learned that simply using `Thread.Sleep()` can make the game feel sluggish. Using a timer-based approach provided much smoother movement.
* **Cursor Management:** Hiding the console cursor (`Console.CursorVisible = false`) was a small detail that massively improved the visual polish of the game.

### 💻 How to Run
1.  Open the solution in Visual Studio.
2.  Press **F5** to run.
3.  Use **Arrow Keys** to control the snake.
