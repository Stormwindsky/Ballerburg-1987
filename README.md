# About Ballerburg (1987)

Ballerburg is a video game created in April 1987 by Eckhard Kruse. In 2004, the game’s creator voluntarily released it into the public domain, so here is a version of the original source code published on a GitHub repository.



For more information about the game, here are some sources:

### Wikipedia:

https://en.wikipedia.org/wiki/Ballerburg


### The official website of the game's creator (available in German only), & also this is where I downloaded the game and the source code:

https://www.eckhardkruse.net/atari_st/baller.html


# Readme.txt english translated:
#### WARNING: THE TEXT BELOW WAS NOT WRITTEN BY ME BUT BY ITS ORIGINAL AUTHOR. IT IS INCLUDED IN THE SOURCE CODE, BUT I HAVE TRANSLATED IT INTO ENGLISH AND CONVERTED IT TO .MD FORMAT SINCE IT WAS ORIGINALLY IN .TXT FORMAT. I HAVE STILL INCLUDED THE ORIGINAL .txt VERSION FOR HISTORICAL PURPOSES.

###### _____________________________________________________________________________


# BALLERBURG (1989) - README

[cite_start]First of all, thank you again for the 20 DM[cite: 1]. [cite_start]You can be proud of yourself, as you have made your own small contribution to helping the principle of Public Domain software gain further ground[cite: 1].

[cite_start]Here are the details regarding the files transferred to this disk[cite: 1]:

---

## 🚀 What's New in the '89 Version
[cite_start]There is now an **'89 version of Ballerburg** (BALLER.PRG)[cite: 1, 2]. [cite_start]The source code provided refers to this extended version[cite: 2].

### Improvements over the predecessor:
* [cite_start]**Compatibility:** There are no longer issues with Blitter-TOS or TOS 1.4 (hopefully)[cite: 3].
* [cite_start]**Multiplayer:** Results for up to six players can now be saved in a table[cite: 3].
* [cite_start]**Game Options:** New options have been added, such as setting a maximum number of rounds to determine the winner based on the score[cite: 3].

---

## 💻 Technical Information (Source Code)
[cite_start]The source code consists of the main files **BALLER1.C** and **BALLER2.C**, as well as **MUSIK.C** (routines for playing **BALLER.MUS**) and the header file **BALLER.H**[cite: 4].

[cite_start]The listings are written for **Lattice C by Metacomco**[cite: 4]. Please note the following for compilation:

1. [cite_start]**Data Types:** Unlike most other compilers, the `int` type is 32-bit and `short` is 16-bit[cite: 4].
2. [cite_start]**Memory Management:** Lattice C programs reserve almost all memory upon loading to allow for UNIX-like memory management[cite: 5, 6]. [cite_start]This can cause issues with `Malloc` or resource loading[cite: 6].
   * [cite_start]The variable `int _mneed=20000;` is used to reduce this automatic reservation[cite: 6].
   * [cite_start]These 20K are used by the `m_laden()` routine[cite: 7].
   * [cite_start]Otherwise, memory is reserved using Gemdos `Malloc`[cite: 8].
3. [cite_start]**Trigonometry:** The code uses double-precision float functions like `atan2(y,x)`, which may not be in every C implementation[cite: 9, 10].
4. [cite_start]**Type Conversions:** Strict casting has been used to ensure correctness and avoid warnings[cite: 11].

---

## 📄 Documentation & Customization
* [cite_start]**Audio:** If you have the Music Editor, you can find the necessary information in **MUSIK.C** to link music into your own programs[cite: 13].
* [cite_start]**Manual:** A detailed manual is included in **ANLEITNG.DOC** (for 1st Word) and **ANLEITNG.TXT** (plain text)[cite: 14].
* [cite_start]**Custom Castles:** You can create your own castles using **BALLER.DAT** as a template, which is heavily commented[cite: 15, 16]. [cite_start]It is recommended to design them on graph paper first[cite: 17].

---

## 📬 Contact
If you have any questions, feel free to contact:

[cite_start]**Eckhard Kruse** [cite: 19]  
[cite_start]Reichenbergweg 7 [cite: 19]  
[cite_start]D-3302 Cremlingen-Weddel [cite: 19]
