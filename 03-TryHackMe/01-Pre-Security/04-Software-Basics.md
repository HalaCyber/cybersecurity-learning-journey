
# Module 4 - Software Basics

## 1. Data Representation

Computers represent and store data using different number systems.

### Number Systems

- **Decimal (Base-10):** Uses digits from `0` to `9`. This is the number system we use in everyday life.
- **Binary (Base-2):** Uses only `0` and `1`. Computers use binary to represent and store data.
- **Hexadecimal (Base-16):** Uses `0-9` and `A-F`. Every 4 bits can be represented by one hexadecimal digit.
- **Octal (Base-8):** Uses digits from `0` to `7`. Every 3 bits can be represented by one octal digit.

### Bits and Bytes

- **1 bit** = `0` or `1`
- **8 bits** = `1 byte`
- **4 bits** = `1 hexadecimal digit`
- **3 bits** = `1 octal digit`

### Binary Example

Binary numbers can be converted to decimal using powers of 2.

```text
0001 = 0×2³ + 0×2² + 0×2¹ + 1×2⁰
     = 0 + 0 + 0 + 1
     = 1

0010 = 0×2³ + 0×2² + 1×2¹ + 0×2⁰
     = 0 + 0 + 2 + 0
     = 2

0011 = 0×2³ + 0×2² + 1×2¹ + 1×2⁰
     = 0 + 0 + 2 + 1
     = 3
````

---

## 2. RGB and Color Representation

Computers can represent colors using **RGB (Red, Green, and Blue)**.

Each color channel has a value between `0` and `255`.

```text
Red   = 1 byte = 8 bits
Green = 1 byte = 8 bits
Blue  = 1 byte = 8 bits

Total = 3 bytes = 24 bits
```

Each channel has:

```text
2⁸ = 256 possible values
```

Therefore, RGB can represent:

```text
256 × 256 × 256 = 16,777,216 colors
```

### Hexadecimal Colors

Each hexadecimal digit represents **4 bits**.

Since an RGB color contains 24 bits:

```text
24 bits ÷ 4 = 6 hexadecimal digits
```

For example:

```text
Binary:
10100011 11101010 00101010

Hex:
A3 EA 2A

RGB Hex:
#A3EA2A
```

A common example is:

```text
#FF0000 = Red
```

---

# 3. Data Encoding

Computers store information using binary, but text requires a system that maps characters to numbers.

## ASCII

**ASCII (American Standard Code for Information Interchange)** is an early character encoding standard.

ASCII uses **7 bits**, allowing:

```text
2⁷ = 128 characters
```

It represents English letters, numbers, punctuation, and control characters.

Examples:

```text
A = 65 decimal = 41 hex
a = 97 decimal = 61 hex
0 = 48 decimal = 30 hex
```

For example:

```text
TryHackMe
```

can be represented in hexadecimal as:

```text
54 72 79 48 61 63 6B 4D 65
```

### Limitations of ASCII

ASCII was mainly designed for English characters, so it could not represent many characters used in other languages.

Several 8-bit character encodings were created to support additional characters, such as:

* ISO-8859-1
* ISO-8859-2

Different encodings could represent the same byte values as different characters, which could cause text to display incorrectly.

---

# 4. Unicode

**Unicode** was created to provide a universal standard for representing characters from different languages and writing systems.

Each character is assigned a unique **code point**.

Examples:

```text
A  → U+0041
Ω  → U+03A9
あ → U+3042
ب  → U+0628
```

### Unicode Encodings

Unicode characters can be encoded using different formats:

* **UTF-8:** Uses 1–4 bytes and is widely used on the web.
* **UTF-16:** Uses 2 or 4 bytes.
* **UTF-32:** Uses 4 bytes.

### Important Difference

**Unicode identifies the character using a code point.**

**UTF-8, UTF-16, and UTF-32 define how that character is encoded and stored.**

---

# 5. JavaScript and Databases

The room briefly introduces JavaScript before moving to database concepts.

The next topic is **Database Basics**, where SQL is introduced.

A **relational database** can be thought of as a collection of related tables.

---

# 6. SQL Basics

**SQL (Structured Query Language)** is used to interact with relational databases.

SQL can be used to retrieve, filter, sort, and modify data.

A **query** is a request made to a database.

### SQL Keywords Learned

#### SELECT

Used to choose which data to display.

```sql
SELECT name
```

#### FROM

Used to specify the table where the data comes from.

```sql
SELECT name
FROM users;
```

#### WHERE

Used to filter records based on a condition.

```sql
SELECT name
FROM users
WHERE age > 18;
```

#### ORDER BY

Used to sort the results.

```sql
SELECT name
FROM users
ORDER BY name;
```

### Important Note

The `SELECT` queries learned in this module retrieve data without changing it.

SQL as a whole can also modify data using commands such as:

* `INSERT`
* `UPDATE`
* `DELETE`

---

# Cybersecurity Perspective

Understanding how software represents and processes data is important in cybersecurity.

Important concepts from this module include:

* Binary
* Bits and bytes
* Decimal
* Hexadecimal
* RGB
* ASCII
* Unicode
* UTF-8
* Character encoding
* SQL
* Databases
* SQL queries

These concepts provide a foundation for understanding how computers store, process, and communicate information.
