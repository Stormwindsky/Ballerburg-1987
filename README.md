# About Ballerburg (1987)

Ballerburg is a video game created in April 1987 by Eckhard Kruse. In 2004, the game's creator voluntarily released it into the public domain, so here is a version of the original source code published on a GitHub repository.

For more information about the game, here are some sources:

### Wikipedia:

https://en.wikipedia.org/wiki/Ballerburg

### The official website of the game's creator (available in German only), & also this is where I downloaded the game and the source code:

https://www.eckhardkruse.net/atari_st/baller.html

---

# Readme.txt (English Translation)

> **WARNING:** THE TEXT BELOW WAS NOT WRITTEN BY ME BUT BY ITS ORIGINAL AUTHOR. IT IS INCLUDED IN THE SOURCE CODE, BUT I HAVE TRANSLATED IT INTO ENGLISH AND CONVERTED IT TO .MD FORMAT SINCE IT WAS ORIGINALLY IN .TXT FORMAT. I HAVE STILL INCLUDED THE ORIGINAL .txt VERSION FOR HISTORICAL PURPOSES.

---

# BALLERBURG (1989) - README

First of all, thank you again for the 20 DM. You can be proud of yourself, as you have made your own small contribution to helping the principle of Public Domain software gain further ground.

Here are the details regarding the files transferred to this disk:

---

## 🚀 What's New in the '89 Version

There is now an **'89 version of Ballerburg** (BALLER.PRG). The source code provided refers to this extended version.

### Improvements over the predecessor:
* **Compatibility:** There are no longer issues with Blitter-TOS or TOS 1.4 (hopefully).
* **Multiplayer:** Results for up to six players can now be saved in a table.
* **Game Options:** New options have been added, such as setting a maximum number of rounds to determine the winner based on the score.

---

## 💻 Technical Information (Source Code)

The source code consists of the main files **BALLER1.C** and **BALLER2.C**, as well as **MUSIK.C** (routines for playing **BALLER.MUS**) and the header file **BALLER.H**.

The listings are written for **Lattice C by Metacomco**. Please note the following for compilation:

1. **Data Types:** Unlike most other compilers, the `int` type is 32-bit and `short` is 16-bit.
2. **Memory Management:** Lattice C programs reserve almost all memory upon loading to allow for UNIX-like memory management. This can cause issues with `Malloc` or resource loading.
   * The variable `int _mneed=20000;` is used to reduce this automatic reservation.
   * These 20K are used by the `m_laden()` routine.
   * Otherwise, memory is reserved using Gemdos `Malloc`.
3. **Trigonometry:** The code uses double-precision float functions like `atan2(y,x)`, which may not be in every C implementation.
4. **Type Conversions:** Strict casting has been used to ensure correctness and avoid warnings.

---

## 📄 Documentation & Customization

* **Audio:** If you have the Music Editor, you can find the necessary information in **MUSIK.C** to link music into your own programs.
* **Manual:** A detailed manual is included in **ANLEITNG.DOC** (for 1st Word) and **ANLEITNG.TXT** (plain text).
* **Custom Castles:** You can create your own castles using **BALLER.DAT** as a template, which is heavily commented. It is recommended to design them on graph paper first.

---

## 📬 Contact

If you have any questions, feel free to contact:

**Eckhard Kruse**  
Reichenbergweg 7  
D-3302 Cremlingen-Weddel
