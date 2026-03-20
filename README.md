# Filter — BMP Image Processing in C

A command-line tool for applying image filters to 24-bit BMP files, built as part of **CS50 (Harvard University)**.

---

## Overview

Digital images can be represented as grids of pixels, each storing intensity values for **Red**, **Green**, and **Blue** channels. In the **24-bit BMP** format, each channel occupies 8 bits, yielding 16,777,216 possible colors per pixel.

This project implements four image filters by directly manipulating the RGB values of each pixel in a BMP file, with all core logic contained in `helpers.c`.

---

## Project Structure
```
filter/
├── bmp.h         # BMP file format structs and type definitions
├── filter.c      # Entry point: I/O handling and filter dispatch
├── helpers.h     # Function prototypes for all filters
├── helpers.c     # Filter implementations (grayscale, sepia, reflect, blur)
└── Makefile      # Build configuration
```

---

## Filters

| Flag | Filter     | Description                                              |
|------|------------|----------------------------------------------------------|
| `-g` | Grayscale  | Converts each pixel to a shade of gray using channel averaging |
| `-s` | Sepia      | Applies a warm, brownish tone using the sepia formula    |
| `-r` | Reflect    | Mirrors the image horizontally                           |
| `-b` | Blur       | Smooths the image using a box blur (3×3 kernel)          |

---

## Usage

**1. Compile**
```bash
make filter
```

**2. Run with a chosen filter**
```bash
./filter -[flag] input.bmp output.bmp
```

**Examples**
```bash
./filter -g images/yard.bmp out.bmp   # Grayscale
./filter -s images/yard.bmp out.bmp   # Sepia
./filter -r images/yard.bmp out.bmp   # Reflect
./filter -b images/yard.bmp out.bmp   # Blur
```

The processed image is saved to the specified output file (e.g., `out.bmp`).

---

## Learning Objectives

This project reinforces the following concepts in C:

- Manipulation of **2D arrays** to represent pixel grids
- Use of **structs** to model BMP headers and pixel data
- Reading and writing **binary files**
- Implementation of **image processing algorithms** from scratch

---

## Reference

Based on the Problem Set from [CS50x — Introduction to Computer Science](https://cs50.harvard.edu/x/), Harvard University.
