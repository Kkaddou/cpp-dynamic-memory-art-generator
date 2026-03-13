# cpp-dynamic-memory-art-generator
C++ project exploring dynamic memory management, deep copying, and 2D array structures, with memory-leak detection using Valgrind.
# C++ Dynamic Memory Management – Digital Art Generator

## Project Overview

This project implements a C++ class that represents a digital artwork composed of randomly generated color values.
Each artwork stores its color data in a dynamically allocated **2D array**, where each cell represents a pixel color code.

The main goal of the project was to practice **manual memory management in C++**, including correct implementation of the *Rule of Three* (copy constructor, assignment operator, and destructor).

The project was developed in a Linux environment and tested using **Valgrind** to verify that no memory leaks or invalid memory accesses occur.

Project Link : https://swe.umbc.edu/~donyaee/current/projects/proj0.html

⚠️ The full source code cannot be published because it belongs to a university coursework repository. This repository documents the architecture, testing strategy, and concepts used.

---

## Key Concepts Practiced

* Dynamic memory allocation (`new` / `delete`)
* Deep vs shallow copying 
* The Rule of Three in C++   ("Destructor, Copy constructor, Copy assignement operato"
* 2D dynamic arrays
* Unit testing design
* Linux development workflow
* Memory debugging using Valgrind

---

## Class Architecture

### Random Class

Provided utility class used to generate random color codes.

* Generates integers between **10 and 99**
* Used to populate the artwork grid

### Art Class

Represents a digital artwork stored as a dynamically allocated 2D array.

Key operations implemented:

* Default constructor (empty object)
* Parameterized constructor
* Destructor
* Copy constructor (deep copy)
* Assignment operator with self-assignment protection
* Dynamic resizing during append operations

---

## Core Features Implemented

### Artwork Generation

Random color values are generated and inserted into the artwork grid.

### Horizontal Append

Two artworks can be combined **left-to-right** if they have matching heights.

### Vertical Append

Two artworks can be combined **top-to-bottom** if they have matching widths.

### Reverse Operation

Reverses the color layout of the artwork.

### Rotation

Rotates the artwork when dimensions allow valid transformation.

---

## Testing Strategy

A dedicated **Tester class** was implemented to verify correctness.

Test coverage includes:

* Constructor error cases (negative dimensions)
* Edge cases (1×1 artwork)
* Deep copy validation
* Assignment operator correctness
* Self-assignment protection
* Append operations
* Reverse and rotate operations

Each test function returns a **pass/fail boolean** and is executed from `main()`.

---

## Memory Leak Detection

The program was executed using **Valgrind** to verify memory safety.

To confirm that all dynamically allocated memory is properly released.

---

## Development Environment

* Language: C++
* Platform: Linux
* Compiler: g++
* Debugging tool: Valgrind

---

## What I Learned

* Designing classes that manage dynamic memory safely
* Avoiding shallow copy errors in pointer-based data structures
* Using Valgrind to diagnose memory leaks and invalid access
* Writing structured unit tests in C++
* Working with remote Linux servers for compilation and testing

---

## Future Improvements

Possible extensions include:

* Using modern C++ (`std::vector`) instead of raw pointers
* Adding image export functionality
* Parallel generation of artwork patterns
* Visualizing the artwork using a GUI or web interface
