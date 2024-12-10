# 0x01. Caching 💾

![Python](https://img.shields.io/badge/Python-3.7-blue?style=flat-square&logo=python) ![Back-End](https://img.shields.io/badge/Back--End-Caching-lightgrey?style=flat-square&logo=backend)

## 📖 Project Overview
In this project, you’ll implement and explore different **caching algorithms** such as FIFO, LRU, LFU, and MRU. These algorithms are critical for optimizing data retrieval and storage in software systems.

## 🎯 Learning Objectives
- 💡 Understand what a caching system is and its purpose.
- 🚀 Learn the differences between FIFO, LIFO, LRU, MRU, and LFU caching algorithms.
- 🧠 Implement caching algorithms using Python.
- 🛠️ Handle edge cases and system limitations of caching systems.

## 🛠️ Technologies Used
- ![Python](https://img.shields.io/badge/Python-3.7-blue?style=flat-square&logo=python) **Python 3.7** on **Ubuntu 18.04 LTS**
- **PEP 8** (v2.5) for code style and formatting.

## 📋 Requirements
- All files must run on **Ubuntu 18.04 LTS** using `python3` (version 3.7).
- Files should start with `#!/usr/bin/env python3`.
- Code must adhere to **PEP 8** standards.
- No external libraries or modules may be imported.
- All functions, modules, and classes must have comprehensive documentation.

## 🚀 Installation and Usage

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/Alogyn/alx-backend.git
    cd alx-backend/0x01-caching
    ```

2. **Run a Test Script**:
    ```bash
    ./0-main.py
    ```

## 📚 Tasks

### 0. Basic Cache 🗂️
Create a class `BasicCache` that inherits from `BaseCaching` and implements a basic caching system without any limit.

### 1. FIFO Cache 📥
Create a class `FIFOCache` that inherits from `BaseCaching` and implements a caching system using the **First In, First Out (FIFO)** algorithm.

### 2. LIFO Cache 📤
Create a class `LIFOCache` that inherits from `BaseCaching` and implements a caching system using the **Last In, First Out (LIFO)** algorithm.

### 3. LRU Cache 🔄
Create a class `LRUCache` that inherits from `BaseCaching` and implements a caching system using the **Least Recently Used (LRU)** algorithm.

### 4. MRU Cache 🔁
Create a class `MRUCache` that inherits from `BaseCaching` and implements a caching system using the **Most Recently Used (MRU)** algorithm.

### 5. LFU Cache 🔢
Create a class `LFUCache` that inherits from `BaseCaching` and implements a caching system using the **Least Frequently Used (LFU)** algorithm.

## 🌐 Resources
- [Cache replacement policies - FIFO](https://en.wikipedia.org/wiki/Cache_replacement_policies#First_In_First_Out_%28FIFO%29)
- [Cache replacement policies - LIFO](https://en.wikipedia.org/wiki/Cache_replacement_policies#Last_In_First_Out_%28LIFO%29)
- [Cache replacement policies - LRU](https://en.wikipedia.org/wiki/Cache_replacement_policies#Least_Recently_Used_%28LRU%29)
- [Cache replacement policies - MRU](https://en.wikipedia.org/wiki/Cache_replacement_policies#Most_Recently_Used_%28MRU%29)
- [Cache replacement policies - LFU](https://en.wikipedia.org/wiki/Cache_replacement_policies#Least-Frequently_Used_%28LFU%29)

## ⚖️ License
This project is part of the ALX Software Engineering Program.  
© 2024 ALX. All rights reserved.
