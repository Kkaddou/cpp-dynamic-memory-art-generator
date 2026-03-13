# Testing Strategy

## Overview

To ensure the correctness of the Art class implementation, a dedicated test program was written in a file named `mytest.cpp`. The test program includes a `Tester` class containing individual test functions.

Each test function verifies a specific behavior of the class and returns a boolean value indicating whether the test passed or failed.

The main function executes all tests and reports their results.

---

## Test Categories

The testing approach includes three categories:

### Normal Cases

Tests typical usage scenarios.

Examples:

* Creating an Art object with valid dimensions (e.g., 10 × 10)
* Appending two artworks with matching dimensions
* Rotating a valid artwork

---

### Edge Cases

Tests boundary conditions.

Examples:

* Creating a 1 × 1 artwork
* Copying an empty artwork
* Appending an empty object to a normal object

---

### Error Cases

Tests invalid inputs or operations.

Examples:

* Creating an Art object with negative dimensions
* Attempting to append artworks with mismatched sizes
* Performing operations on empty objects

---

## Deep Copy Verification

To ensure correct implementation of the copy constructor and assignment operator, tests verify:

* The copied object has the same dimensions
* The color values match
* The memory locations are different (ensuring a deep copy)

---

## Example Test Algorithm

Example logic used when testing the copy constructor:

1. Create an Art object with valid dimensions.
2. Generate random color values.
3. Create a copy using the copy constructor.
4. Verify both objects have identical dimensions.
5. Verify all color values match.
6. Confirm both objects use different memory addresses.

---

## Tools Used

Testing was performed using:

* Custom test functions implemented in the `Tester` class
* Linux command-line compilation using `g++`
* Valgrind for memory leak detection
