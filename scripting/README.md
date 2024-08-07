<h1>
  <span class="headline">Python Modules and Scripting</span>
  <span class="subhead">Scripting</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to create Python scripts that automate tasks by taking input, interacting with files, and leveraging external libraries, such as csv, to manage data.

| Lesson    | Duration |
| --------- | -------- |
| Scripting | 50 min   |

## Putting It All Together

Armed with the foundational building blocks of Python, we can start creating genuinely useful scripts to automate specific tasks, like:

- Filing analysis.
- Sending reporting emails.
- Formatting files.
- Processing data.

![Image Placeholder](TKTK)

## What’s a Script?

When people refer to **scripts**, they usually mean code that:

- Takes input.
- Gives output.
- Reads or writes to a file.
- Performs a task.

We have "Performs a task" down! Let’s look at how we can build useful tools in Python by combining these other layers in our programs.

> 🍎 One of the strongest use cases for Python is writing helpful scripts to automate work tasks or create helpful tools for yourself. Scripting will open up our ability to interact with files and provide meaningful input to our Python code; in other words, to start building useful things!

## Input From Users and Files

| **User Input**                                                                              |
| ------------------------------------------------------------------------------------------- |
| Prompt users to type in a response to given text, then process that response as a variable. |

```python
name = input("Type your name: ")

# the script pauses to wait

# continues when user submits

print(name)
```

| **File Input**                                                      |
| ------------------------------------------------------------------- |
| Access the contents of a specific file from within a Python script. |

```python
log = open("./log.txt", "w")

# opens log.txt in 'write' mode

log.write("Another great day!")

# writes to the end of the file

log.close()
```

## Open for Business

When accessing files, you need to specify the “mode” in which the file should be opened.

You must also be sure to close the file after working with it. Use the following pattern to let Python do that for you automatically:

```python
with open("log.txt", "a") as log:
    log.write("All clear.")
```

| **Mode** | **Description**                             |
| -------- | ------------------------------------------- |
| `'r'`    | Read-only mode.                             |
| `'w'`    | Write.                                      |
| `'a'`    | Append new contents to the end of the file. |
| `'+'`    | Add to any mode to include read and write.  |

## Partner Exercise: 6.3 So Much to Do... 10 min TKTK

Add a comment to each line of the “to-do list” script in **Section 6.3** of the notebook.

![Image Placeholder](TKTK)

## With These Powers Combined...

Managing files manually can get a bit awkward. Fortunately, there are plenty of **modules** out there to make things easier — especially for common file and data formats like `.csv`!

Let’s explore a basic module called **"csv"** for just this purpose.

![Image Placeholder](TKTK)

## Discussion: What Are Spreadsheets Made Of? TKTK

Before we start manipulating `.csv` files in Python, let’s reflect:

- What Python data structure might be best for storing a `.csv` row ID and the data in the corresponding row in the `.csv` file?

<br>

<details>
<summary>✅ Click to see the answer: </summary>
<hr>

A dictionary is best, because it is a set of key (row ID) and value (the data corresponding to that row) pairs.

</details>

<br>

Before we start manipulating `.csv` files in Python, let’s reflect:

- What Python data structures might be best for representing a whole table of rows?

<br>

<details>
<summary>✅ Click to see the answer: </summary>
<hr>

A list of dictionaries, because a list preserves the order of the rows.

</details>

## Discussion: Reading and Writing TKTK

Let’s explore how we would read and write to a `.csv` file by consulting the [documentation for the csv library](https://docs.python.org/3/library/csv.html#).

Consider:

1. How can we read a row from a `.csv` file?
2. How can we write a new row to an existing `.csv` file?
3. How can we modify the existing rows of a `.csv` file?

Take a few minutes to explore the documentation before we discuss the answers. This will help you find relevant examples and better understand the material.

Remember, an essential skill when using libraries is learning how to read and interpret their documentation effectively.

## Partner Exercise: 6.4 TPS Reports 20 min TKTK

Let's translate a given list of dictionaries into a `.csv` file using the csv module.

![Image Placeholder](TKTK)

## Discussion: Automating With Python TKTK

One of the main uses of Python as a productivity tool is creating reusable scripts to analyze and generate `.csv` files.

**_What regularly scheduled processes can you anticipate creating a Python analysis script for, either for your own role or to enhance the productivity of another team member?_**

## Solo Exercise: 6.5 Ultimate RPS Challenge 20 min TKTK

As a bonus challenge, let’s use our `.csv`-writing abilities to keep track of all of the games played from a command line version of Rock, Paper, Scissors.

_If you are not able to finish this exercise in the given class time, we encourage you to complete it as homework._
