# LeetCode 192 - Tenth Line

## Problem

Given a text file named `file.txt`, print only the **10th line** of the file.

The solution should print the exact contents of the 10th line.

## Example

### Input

Suppose `file.txt` contains:

```text
Line 1
Line 2
Line 3
Line 4
Line 5
Line 6
Line 7
Line 8
Line 9
Line 10
Line 11
```

### Output

```text
Line 10
```

## Approach

This problem is a **Shell** problem rather than a Python or SQL problem.

The `sed` command can be used to select a specific line from a text file.

The command is:

```bash
sed -n '10p' file.txt
```

## Explanation of the Command

### `sed`

`sed` stands for **Stream Editor**.

It is commonly used for processing and modifying text.

### `-n`

The `-n` option prevents `sed` from printing every line automatically.

### `10p`

This tells `sed` to:

* `10` → select line number 10
* `p` → print that line

### `file.txt`

This is the input text file.

Therefore:

```bash
sed -n '10p' file.txt
```

means:

**Print only the 10th line from `file.txt`.**

## Alternative Solution

Another possible solution is:

```bash
awk 'NR==10' file.txt
```

Here:

* `awk` processes the file line by line.
* `NR` represents the current line number.
* `NR==10` selects the 10th line.

## Key Concept

The main concept is **command-line text processing**.

The simplest solution is:

```bash
sed -n '10p' file.txt
```

## Time Complexity

**O(n)**

The command processes the input file to locate the required line.

## Space Complexity

**O(1)** auxiliary space in the typical streaming model.

Only the necessary information for processing the file is maintained.

## Difficulty

**Easy**

## Topics

* Shell
* Linux Commands
* `sed`
* `awk`
* Text Processing
* File Processing

## What I Learned

This problem introduced basic Shell commands for processing text files.

I learned how the `sed` command can be used to select and print a specific line from a file.

The key command is:

```bash
sed -n '10p' file.txt
```

## Author

T.Nandhini
