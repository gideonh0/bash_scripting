# Day 1: The Basics (Shebang, Variables, & Input)

## 1. The Shebang (`#!`)
The first line of any script. It directs the system to the correct interpreter.
* `#!/bin/bash`: Direct path to the bash binary.
* `#!/usr/bin/env bash`: More portable; finds bash in the user's current environment.

## 2. Naming Conventions
We use three primary styles for different purposes:

| Style | Example | Common Use Case |
| :--- | :--- | :--- |
| **Snake_Case** | `User_name` | Standard local variables. |
| **camelCase** | `tempFile` | Local variables (less common in Bash, but used). |
| **ALL_CAPS** | `API_KEY` | Environment variables or global constants. |

## 3. Accessing Variables: `$` vs `${}`
Both access the value of a variable, but `${}` (parameter expansion) provides safety and clarity.

* **`$variable`**: Quick and easy for simple strings.
* **`${variable}`**: Required when the variable is followed by characters that might confuse the interpreter <br>`${user_name}_file` It also allows for advanced string manipulation later on.

## 4. Execution vs. Sourcing
There are two primary ways to run a `.sh` file:

| Differences | Execution | Sourcing |
| :--- | :--- | :--- |
| Permission | Requires "execute" permissions: <br>`chmod +x script.sh`. | Does **not** require execute permissions. |
| Runs In | a **sub-shell** (a new process).  | the **current shell** process. |
| Variable retain | do **not** persist in your current terminal after it finishes. | **will remain** in your terminal environment after the script ends. |
| Code | `./script.sh` | `source script.sh` or `. script.sh` |
