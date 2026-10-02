# Ex.No.6 AI-Assisted Programming and Debugging

## Date:
07-09-2026

## Register No:
212225060250

## Aim

To write and implement Python code that integrates with multiple AI tools to automate API interaction, compare AI-generated outputs, identify and fix bugs, optimize code, analyze time and space complexity, generate unit tests, and compare manual coding with AI-assisted coding.

---

## AI Tools Required

1. ChatGPT / OpenAI API
2. Google Gemini API
3. Python 3.x
4. Python packages:
   - `openai`
   - `google-genai`
   - `python-dotenv`
   - `pytest`

---

## Explanation

AI-assisted programming uses Artificial Intelligence tools to support software development activities such as code generation, debugging, optimization, explanation, and testing.

In this experiment, multiple AI tools are used to solve the same programming task. Their outputs are collected and compared to identify differences in correctness, clarity, efficiency, and code quality.

The experiment follows these stages:

1. Define a programming problem.
2. Generate a solution using multiple AI tools.
3. Compare the generated solutions.
4. Identify bugs and weaknesses.
5. Optimize the code.
6. Analyze time and space complexity.
7. Generate unit tests.
8. Compare manual coding with AI-assisted coding.
9. Analyze the overall code quality.

---

# Problem Statement

Develop a Python program that analyzes a list of student marks and produces:

- The highest mark
- The lowest mark
- The average mark
- The number of students who passed
- The number of students who failed

The program should also validate the input and handle invalid or empty data appropriately.

---

# AI Persona Pattern

The AI tools are instructed to act as experienced Python programmers and code reviewers.

### Persona Prompt

> Act as an experienced Python programmer and code reviewer. Write clean, readable and efficient Python code. Validate the input, handle edge cases, explain the time and space complexity, identify possible bugs, and generate suitable unit tests.

---

# Initial Prompt

The following prompt was given to multiple AI tools:

> Act as an experienced Python programmer. Write a Python program that accepts a list of student marks and calculates the highest mark, lowest mark, average mark, number of passed students and number of failed students. Assume that marks of 40 or above are passing marks. Provide readable code and explain the solution briefly.

---

# AI Tool 1 – OpenAI

The OpenAI API can be accessed from Python using the official OpenAI SDK and the Responses API.

### Example Code

```python
from openai import OpenAI

client = OpenAI()

prompt = """
Act as an experienced Python programmer.

Write a Python program that accepts a list of student marks and calculates:
1. Highest mark
2. Lowest mark
3. Average mark
4. Number of passed students
5. Number of failed students

A mark of 40 or above is considered a pass.

Use clean and readable Python code.
"""

response = client.responses.create(
    model="gpt-5",
    input=prompt
)

print(response.output_text)
