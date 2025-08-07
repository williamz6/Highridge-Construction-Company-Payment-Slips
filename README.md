# Worker Payment Slip Generator(Python version)

This Python program generates payment slips for **400 dynamically created workers**, assigning each an appropriate **employee level** based on their **salary** and **gender**, using **conditional logic** and **exception handling**.

---

## 📌 Features

* **Dynamic Worker List**: Creates a list of 400 workers, each with randomly assigned salary and gender.
* **Payment Slip Generation**: Iterates through each worker to print a structured payment slip.
* **Conditional Employee Level Assignment**:

  * Level **A1**: Salary between \$10,000 and \$20,000.
  * Level **A5-F**: Salary between \$7,500 and \$30,000 **and** gender is female.
* **Error Handling**: Includes exception handling for both worker creation and payment slip generation to ensure robust execution.

---

## 🔁 Workflow Summary

### Step 1: Program Implementation

A Python program was developed to simulate a realistic payroll scenario, fulfilling all assignment requirements.

### Step 2: List Creation

A list of **400 workers** is dynamically generated using a `for` loop. Each worker has:

* A unique name (e.g., `Worker1`, `Worker2`, …)
* A randomly assigned gender (`Male` or `Female`)
* A randomly generated salary between `$5,000` and `$32,000`
* Level(`unassigned`, `A1`, `A5-F`)

### Step 3: Loop for Payment Slips

Another `for` loop iterates through the list to:

* Read each worker’s information
* Assign employee level based on conditions
* Print the payment slip in a clear format

### ✅ Step 4: Conditional Statements

Two primary conditions are implemented:

```python
if 10000 < salary < 20000:
    level = "A1"
elif 7500 < salary < 30000 and gender == "Female":
    level = "A5-F"
```

### ✅ Step 5: Exception Handling

Try/except blocks are used:

* While **creating** each worker
* While **generating** each payment slip
  This ensures the program can handle issues like missing data or unexpected errors gracefully.

---

## 🚀 How to Run

1. Save the script in a `.py` file (e.g., `payroll_generator.py`)
2. Run using Python 3:

```bash
python payroll_generator.py
```

---

## 🛠️ Dependencies

* No external libraries required.
* Uses Python's built-in `random` module.

---

## 🧠 Notes

* If a salary meets both conditions, **"A1"** takes precedence due to the `if-elif` structure.
* All gender-based comparisons are case-sensitive (`"Female"` is expected exactly).

## Converted Python code to R

## Worker Payroll Slip Generator (R version)

## Overview

This R script generates a list of workers, assigns them random genders and salaries, categorizes them into employee levels based on salary and gender criteria, and prints out a **payment slip** for each worker. It uses basic R structures like lists, loops, conditionals, and error handling.

## Features

* Creates **400 workers** with:

  * **Name** in the format: `worker_1`, `worker_2`, ..., `worker_400`.
  * **Gender** randomly assigned as `"Male"` or `"Female"`.
  * **Salary** randomly assigned between `$5,000` and `$32,000`.
* Determines **employee level**:

  * **A1** → Salary between \$10,000 and \$20,000.
  * **A5-F** → Salary between \$7,500 and \$30,000 **and** gender is Female.
  * Defaults to `"Unknown"` if no condition matches.
* Prints each worker’s **payment slip** with name, gender, salary, and employee level.
* Includes **error handling** to catch and display any issues during worker creation or payment slip generation.

## How It Works

1. **Worker Generation**

   * A `for` loop runs from 1 to `num_workers` (400 by default).
   * Each worker is stored as a list (`name`, `salary`, `gender`).
   * Errors are caught with `tryCatch()` and logged.

2. **Payment Slip Printing**

   * Iterates through each worker in the `workers` list.
   * Determines the worker’s `level` based on salary and gender rules.
   * Prints the payment slip to the console.

3. **Error Handling**

   * Any issue in creating or printing a worker’s record will display an error message but will not stop the script.

## Example Output

```R
Paymemnt Slip
Name: worker_1
Gender: Female
Salary: $ 12500
Employee Level: A1

Paymemnt Slip
Name: worker_2
Gender: Male
Salary: $ 18000
Employee Level: A1
```

## Requirements

* R version 3.5 or later
* No external packages required (uses base R)

## Usage

1. Copy the script into an `.R` file (e.g., `payroll_generator.R`).
2. Open R or RStudio.
3. Run:

   ```r
   source("payroll_generator.R")
   ```

## Notes

* Salary and gender are **randomly generated** each run, so results will vary.
* The script currently **prints directly to console.**
