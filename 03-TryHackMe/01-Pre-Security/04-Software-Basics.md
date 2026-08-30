Module 4  _  Software Basics :

Data Representation:
--------------------

We learned how computers represent colors using **RGB (Red, Green, and Blue)**. Each color can be represented using different levels of red, green, and blue.

With only two states, **on (1) and off (0)**, RGB can create **8 different colors** because 2 × 2 × 2 = 8.

For millions of colors, each RGB color uses **256 levels**, from 0 to 255. This gives:

**256 × 256 × 256 = 16,777,216 colors.**

Each RGB value needs **8 bits (1 byte)**, so a color uses **24 bits or 3 bytes** in total.

We also learned about **hexadecimal (Hex)**. Every 4 bits can be represented by one hexadecimal digit (0–9 and A–F). Therefore, an RGB color can be written using **6 hexadecimal digits**.

For example:

**Binary:** `10100011 11101010 00101010`
**Hex:** `A3EA2A`

The **Hex Color Converter website** helps us convert colors between **binary, decimal, and hexadecimal** and shows a preview of the color.

0000 = 0 × 23 + 0 × 22 + 0 × 21 + 0 × 20 = 0 × 8 + 0 × 4 + 0 × 2 + 0 × 1 = 0

0001 = 0 × 23 + 0 × 22 + 0 × 21 + 1 × 20 = 0 × 8 + 0 × 4 + 0 × 2 + 1 × 1 = 1

0010 = 0 × 23 + 0 × 22 + 1 × 21 + 0 × 20 = 0 × 8 + 0 × 4 + 1 × 2 + 0 × 1 = 2

0011 = 0 × 23 + 0 × 22 + 1 × 21 + 1 × 20 = 0 × 8 + 0 × 4 + 1 × 2 + 1 × 1 = 3
-----------------
1 bit   = 0 أو 1
8 bits  = 1 byte
4 bits  = 1 Hex digit
3 bits  = 1 Octal digit
----------------------
Red   = 1 byte
Green = 1 byte
Blue  = 1 byte
        ↓
3 bytes = 24 bits
        ↓
16,777,216 possible colors
------------------------------
### Data Representation – Simple Summary

Computers use different number systems to represent and store data:

* **Decimal (Base-10):** Uses numbers from 0 to 9. It is the system we use every day.
* **Binary (Base-2):** Uses only `0` and `1`. Computers use binary to store information.
* **Hexadecimal (Base-16):** Uses `0-9` and `A-F`. Every **4 bits** can be represented by one hexadecimal digit.
* **Octal (Base-8):** Uses `0-7`. Every **3 bits** can be represented by one octal digit.

### Bits, Bytes, and Colors

* **Bit:** A binary digit that can be `0` or `1`.
* **Byte:** 8 bits. It is also called an **octet**.
* **RGB:** Colors are made from **Red, Green, and Blue**.
* Each RGB color uses **1 byte (8 bits)**.
* This gives **256 values for each color** and more than **16 million possible colors**.
* A **Hex color** uses 6 hexadecimal digits, for example: `#FF0000` for red.

The next topic, **Data Encoding**, explains how computers store letters, different languages, and emojis using bits.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
Data Encoding:
--------------
ASCII = American Standard Code for Information Interchange
### ASCII and Text Encoding – Simple Summary

Computers store information using **0s and 1s**. To store text, computers need a system that maps characters to numbers.

**ASCII** is an early character encoding standard. It uses numbers from **0 to 127** to represent English letters, numbers, punctuation, and control characters.

For example:

* `A` = 65 decimal = `41` hex
* `a` = 97 decimal = `61` hex
* `0` = 48 decimal = `30` hex

A word like **TryHackMe** is stored as numbers, which can then be represented in binary or hexadecimal.

Example:

`TryHackMe` → `54 72 79 48 61 63 6B 4D 65` in hexadecimal.

ASCII was mainly designed for English, so it was not enough for many European languages. Other encodings such as **ISO-8859-1** and **ISO-8859-2** were created to support additional characters.

### Unicode – Simple Summary

**ASCII** is a 7-bit encoding standard with **128 characters**. It was mainly designed for English, so it could not represent many characters from other languages.

**Extended ASCII** used 8 bits, but different standards such as ISO-8859-1 and ISO-8859-2 used different character sets. This could cause text to display incorrectly.

**Unicode** was created to provide a universal standard for characters from different languages. Each character has a unique **code point**.

Examples:

* `A` → `U+0041`
* `Ω` → `U+03A9`
* `あ` → `U+3042`
* `ب` → `U+0628`

There are three common Unicode encodings:

* **UTF-8:** Uses 1–4 bytes and is very common on the web.
* **UTF-16:** Uses 2 or 4 bytes.
* **UTF-32:** Always uses 4 bytes.

The important idea is:

**Unicode identifies the character, while UTF-8, UTF-16, and UTF-32 define how the character is stored.**
----------------------------------------------------------------------------------------
JavaScript: Simple Demo:
-------------------------
In the next room, Database Basics, we will explore SQL. Although SQL is not a programming language, it is commonly used to query relational database systems. For now, think of a relational database as a large set of related tables.

Database SQL Basics:
-------------------
SQL is a language used to ask questions of a database.
These questions are called queries.

A query does not change the data. It only displays the requested information from the table.

SQL Queries Learned in This Room

    SELECT – choose what data to display

    FROM – choose where the data comes from

    WHERE – filter records based on a condition

    ORDER BY – sort results
