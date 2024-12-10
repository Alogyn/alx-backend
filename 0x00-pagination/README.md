# 0x00. Pagination 📚

![Python](https://img.shields.io/badge/Python-3.7-blue?style=flat-square&logo=python) ![Backend](https://img.shields.io/badge/Backend-Pagination-green?style=flat-square&logo=backend)

## 📖 Project Overview
This project focuses on implementing various pagination methods for large datasets. The goal is to handle data efficiently by dividing it into smaller, manageable pages. The tasks involve:
- **Simple Pagination**: Using page and page size to retrieve specific slices of the dataset.
- **Hypermedia Pagination**: Returning pagination metadata alongside data.
- **Deletion-Resilient Pagination**: Ensuring consistent data retrieval even after deletions.

# 🎯 Learning Objectives
 Implement pagination using page and page size parameters.
 Design hypermedia pagination with metadata for dynamic navigation.
 Create deletion-resilient pagination to avoid missing items after data changes.

# 🛠️ Technologies Used
 ![Python](https://img.shields.io/badge/Python-3.7-blue?style=flat-square&logo=python) **Python 3.7**
 **CSV Files** for dataset handling
 **PyCodeStyle** (v2.5.*) for code quality

# 📋 Requirements
 Files must run on **Ubuntu 18.04 LTS** using `python3`.
 All files should end with a new line.
 Adhere to **PEP 8** standards.
 Provide module, class, and function-level documentation.
 Include type annotations for all functions and coroutines.

# 🚀 Dataset
 The project uses the `Popular_Baby_Names.csv` file.
 Contains data on baby names, gender, ethnicity, and rankings.

# 📂 Tasks Breakdown
## Task 0: Simple Helper Function
 **File**: `0-simple_helper_function.py`
 Write a function `index_range` that calculates the start and end indices for a given page and page size.
 **Usage**:
 ```python
 res = index_range(1, 7)
 print(res)  # (0, 7)
 ```

## Task 1: Simple Pagination
 **File**: `1-simple_pagination.py`
 Implement a `Server` class to paginate the dataset using `index_range`.
 Define a method `get_page(page, page_size)` to return specific pages of data.
 **Usage**:
 ```python
 server = Server()
 print(server.get_page(1, 3))
 ```

## Task 2: Hypermedia Pagination
 **File**: `2-hypermedia_pagination.py`
 Extend the `Server` class with a `get_hyper` method.
 Include metadata: `page_size`, `page`, `next_page`, `prev_page`, and `total_pages`.
 **Usage**:
 ```python
 server = Server()
 print(server.get_hyper(1, 2))
 ```

## Task 3: Deletion-Resilient Pagination
 **File**: `3-hypermedia_del_pagination.py`
 Implement `get_hyper_index` to ensure continuity after data deletions.
 Return consistent pages based on indexed dataset mapping.
 **Usage**:
 ```python
 server = Server()
 print(server.get_hyper_index(3, 2))
 ```

# 🧾 Example Outputs
## Simple Helper Function
``bash
 ./0-main.py
class 'tuple'>
0, 7)
class 'tuple'>
30, 45)
``
## Simple Pagination
``bash
 ./1-main.py
ssertionError raised with negative values
ssertionError raised with 0
ssertionError raised when page and/or page_size are not ints
['2016', 'FEMALE', 'ASIAN AND PACIFIC ISLANDER', 'Olivia', '172', '1'],
['2016', 'FEMALE', 'ASIAN AND PACIFIC ISLANDER', 'Chloe', '112', '2'],
['2016', 'FEMALE', 'ASIAN AND PACIFIC ISLANDER', 'Sophia', '104', '3']]
[['2016', 'FEMALE', 'ASIAN AND PACIFIC ISLANDER', 'Emily', '99', '4'],
 ['2016', 'FEMALE', 'ASIAN AND PACIFIC ISLANDER', 'Mia', '79', '5']]
[]
```

### Hypermedia Pagination
```bash
$ ./2-main.py
{'page_size': 2, 'page': 1, 'data': [['2016', 'FEMALE', 'ASIAN AND PACIFIC ISLANDER', 'Olivia', '172', '1'],
                                     ['2016', 'FEMALE', 'ASIAN AND PACIFIC ISLANDER', 'Chloe', '112', '2']],
 'next_page': 2, 'prev_page': None, 'total_pages': 9709}
```

### Deletion-Resilient Pagination
```bash
$ ./3-main.py
AssertionError raised when out of range
Nb items: 19418
{'index': 3, 'data': [['2016', 'FEMALE', 'ASIAN AND PACIFIC ISLANDER', 'Emma', '99', '4'],
                      ['2016', 'FEMALE', 'ASIAN AND PACIFIC ISLANDER', 'Emily', '99', '4']],
 'page_size': 2, 'next_index': 5}
{'index': 5, 'data': [['2016', 'FEMALE', 'ASIAN AND PACIFIC ISLANDER', 'Mia', '79', '5'],
                      ['2016', 'FEMALE', 'ASIAN AND PACIFIC ISLANDER', 'Charlotte', '59', '6']],
 'page_size': 2, 'next_index': 7}
```

## 🌐 Resources
- [REST API Design: Pagination](https://www.restapitutorial.com/lessons/restfulresourcenaming.html)
- [HATEOAS](https://en.wikipedia.org/wiki/HATEOAS)

## ⚖️ License
This project is part of the ALX Software Engineering Program.  
© 2024 ALX. All rights reserved.
