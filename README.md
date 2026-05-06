# 📘 Java String & StringBuffer: The Ultimate Revision Guide

This repository is a comprehensive resource designed for digital revision. It covers the core mechanics of String handling in Java, memory management, and includes a dedicated "Interview Drill" for StringBuffer.

---

## 📑 Table of Contents
1. [String Architecture & SCP](#1-string-architecture--scp)
2. [The Immutability Factor](#2-the-immutability-factor)
3. [String vs StringBuilder vs StringBuffer](#3-string-vs-stringbuilder-vs-stringbuffer)
4. [Practical Logic & Code](#4-practical-logic--code)
5. [💎 StringBuffer: 20 Essential Interview Q&A](#5-stringbuffer-20-essential-interview-qa)

---

## 1. String Architecture & SCP
In Java, a **String** is an **Object**. 
- **String Constant Pool (SCP):** A special memory area in the Heap that caches literals to save space.
- **Literal vs New:** `String s1 = "Java"` creates 1 object in SCP. `String s2 = new String("Java")` creates 2 objects (one in Heap, one in SCP).

## 2. The Immutability Factor 🔒
Strings are **immutable** (cannot be changed). 
- **Security:** Prevents sensitive data (passwords, URLs) from being altered.
- **Thread Safety:** Multiple threads can access the same string without corruption.

## 3. String vs StringBuilder vs StringBuffer

| Feature | String | StringBuilder | StringBuffer |
| :--- | :--- | :--- | :--- |
| **Mutability** | Immutable | **Mutable** | **Mutable** |
| **Performance** | Slow (new objects) | **Fastest** | Moderate |
| **Thread Safe** | Yes | No | **Yes (Synchronized)** |

---

## 4. Practical Logic & Code

### A. Palindrome Logic
```java
String clean = str.toLowerCase();
String rev = new StringBuilder(clean).reverse().toString();
boolean isPalindrome = clean.equals(rev);
```

### B. Efficient Manipulation
Always use `StringBuilder` or `StringBuffer` inside loops to avoid memory leaks caused by creating thousands of String objects.

---

## 5. 💎 StringBuffer: 20 Essential Interview Q&A

1. **What is StringBuffer?**  
   A mutable class in Java used to create modifiable strings without creating new objects.
2. **Why is StringBuffer used?**  
   To improve performance when strings are modified frequently.
3. **Is StringBuffer mutable or immutable?**  
   **Mutable.**
4. **Is StringBuffer thread-safe?**  
   **Yes.** All methods are synchronized.
5. **Where is StringBuffer stored?**  
   In **Heap memory** (not SCP).
6. **What is the default capacity?**  
   **16 characters.**
7. **What is capacity?**  
   The total number of characters stored before resizing occurs.
8. **How does capacity grow?**  
   Formula: `(oldCapacity * 2) + 2`.
9. **Difference between length() and capacity()?**  
   `length()` is actual characters; `capacity()` is total allocated space.
10. **What happens when capacity exceeds?**  
    A larger array is created and data is copied over.
11. **What is append()?**  
    Adds data to the end of the existing object.
12. **What is insert()?**  
    Adds data at a specific index.
13. **What is delete()?**  
    `delete(start, end)` removes characters from start to end-1.
14. **What is replace()?**  
    Replaces a portion of the string with another.
15. **What is reverse()?**  
    Reverses the character sequence in the object.
16. **How to convert StringBuffer to String?**  
    Use `sb.toString();`.
17. **Difference between StringBuffer and StringBuilder?**  
    StringBuffer is **thread-safe (slower)**; StringBuilder is **not thread-safe (faster)**.
18. **Why is StringBuffer slower?**  
    Due to the overhead of **synchronization**.
19. **What type of synchronization is used?**  
    Method-level synchronization.
20. **When should you use StringBuffer?**  
    When multiple threads are modifying the string and data consistency is required.

---
**🚀 Summary:** `StringBuffer` = Mutable + Thread-safe + Moderate performance.

**Author:** [Your Name]
