# 📘 Page Replacement Algorithm Simulator

A Python-based **Operating Systems project** that simulates and compares three classic page replacement algorithms: **FIFO (First-In, First-Out), LRU (Least Recently Used), and Optimal Page Replacement**.

This project demonstrates how operating systems manage memory frames, handle page faults, and evaluate page replacement strategies using performance metrics.

## 👨‍💻 Author Information

* **Name:** Siddh Jain
* **Enrollment No. :** BTE25DTA000039
* **Course:** B.Tech — Data Analytics
* **Project:** Operating Systems Lab
* **Institution:** SAGE University

---

## 📌 Project Overview

Page replacement is an important concept in operating systems and virtual memory management. When a page requested by a process is not available in physical memory, a page fault occurs. If all memory frames are occupied, the operating system must decide which page to replace.

This project implements three page replacement algorithms and compares their performance using page faults, page hits, hit ratios, and fault ratios.

## ✨ Features

* Accepts comma-separated or space-separated page-reference strings.
* Validates user input and frame count.
* Displays step-by-step page replacement operations.
* Shows the contents of memory frames after each page reference.
* Identifies page hits and page faults.
* Displays which page is replaced during a page fault.
* Calculates total page faults and page hits.
* Computes hit ratio and fault ratio.
* Compares FIFO, LRU, and Optimal algorithms.
* Includes manual tracing and custom reference-string experiments.
* Demonstrates Belady's anomaly.

## 🧠 Algorithms Implemented

### 1. FIFO (First-In, First-Out)

FIFO replaces the page that entered memory first.

**Advantages:**

* Simple to understand and implement.
* Requires minimal bookkeeping.

**Limitation:**

* May replace a frequently used page.
* Can suffer from Belady's anomaly.

### 2. LRU (Least Recently Used)

LRU replaces the page that has not been used for the longest period.

**Advantages:**

* Uses recent page-access history.
* Often performs better than FIFO for suitable reference patterns.

**Limitation:**

* Requires additional bookkeeping to track page usage.

### 3. Optimal Page Replacement

Optimal replaces the page whose next use is farthest in the future, or that will not be used again.

**Advantages:**

* Provides a theoretical benchmark for comparing page replacement algorithms.
* Produces the minimum possible number of page faults for a given reference string and frame count.

**Limitation:**

* Requires knowledge of future page references, so it cannot generally be implemented as a practical online algorithm in a real operating system.

---

## 🛠️ Technologies Used

* **Programming Language:** Python
* **Development Environment:** Jupyter Notebook
* **Platform:** GitHub

## 📂 Project Structure

```text
Page-Replacement-Algorithm-Simulator/
│
├── Page_Replacement_Simulator.ipynb
├── page_replacement.py
├── Project_Report.pdf
├── Assignment_Answers.md
├── README.md
│
└── screenshots/
```

*Make sure the filenames and folders match the actual contents of your GitHub repository.*

## ⚙️ Requirements

* Python 3.x
* Jupyter Notebook or Google Colab (for running the notebook)

## 🚀 How to Run the Project

### Method 1: Using Jupyter Notebook

1. Install Python and Jupyter Notebook, or open Google Colab.
2. Open `Page_Replacement_Simulator.ipynb`.
3. Execute the notebook cells in order.
4. Enter the page-reference string when prompted.
5. Enter the number of available memory frames.
6. Review the simulation results for each algorithm.

### Method 2: Using Python

Open a terminal in the project directory and execute:

```bash
python page_replacement.py
```

Example input:

```text
Enter page reference string (comma or space separated): 1 2 3 1 4 2 5
Enter number of frames: 3
```

The program will process the input and display the corresponding results.

## 📊 Performance Metrics

The simulator calculates the following metrics:

| Metric      | Description                                              | Formula                        |
| ----------- | -------------------------------------------------------- | ------------------------------ |
| Page Faults | Number of page references that are not present in memory | Count of page faults           |
| Page Hits   | Number of page references already present in memory      | Count of page hits             |
| Hit Ratio   | Proportion of references that result in hits             | Page Hits / Total References   |
| Fault Ratio | Proportion of references that result in faults           | Page Faults / Total References |

**Relationship:**

`Hit Ratio + Fault Ratio = 1 (or 100%)`

## 🧪 Experiments Included

### Experiment 1: Manual Tracing

Step-by-step simulation of FIFO, LRU, and Optimal using a fixed page-reference string and three memory frames.

### Experiment 2: Belady's Anomaly

Demonstrates how FIFO can produce more page faults even when the number of memory frames increases.

### Experiment 3: Custom Reference Strings

Compares FIFO and LRU using different page-reference sequences to observe how algorithm performance changes with the input.

## 📈 Sample Results

For the reference string:

`1 2 3 1 4 2 5`

With **3 memory frames**, the sample results documented in the project are:

| Algorithm | Page Faults | Page Hits |
| --------- | ----------: | --------: |
| FIFO      |           5 |         2 |
| LRU       |           6 |         1 |
| Optimal   |           5 |         2 |

Run the program with the same input to verify the results against your current implementation.

## 🎯 Learning Outcomes

Through this project, I explored:

* Virtual memory and page replacement concepts.
* Implementation of operating system algorithms using Python.
* Memory frame management and page replacement decisions.
* Calculation of page faults, page hits, and performance ratios.
* Comparison of algorithm efficiency using reference strings.
* The concept of Belady's anomaly.
* Project documentation and version control using GitHub.

## 🔮 Future Enhancements

* Add graphical comparisons of page faults and hit ratios.
* Develop an interactive web-based interface.
* Implement additional algorithms, such as Second-Chance and Clock.
* Add automated test cases for different reference strings.
* Improve visualization of memory-frame changes during simulation.

## 👨‍🎓 About the Author

**Siddh Jain**
B.Tech — Data Analytics
SAGE University

This project was developed as part of my Operating Systems Lab work to strengthen my understanding of memory management and page replacement algorithms.

---

⭐ **If you find this project useful, feel free to explore the code and learn more about operating system memory management.**
