# Recording Script — Variables & Data Types

**Channel:** Code AI with Yogesh  
**Public episode:** 1 (episode 2 in the original plan)  
**Title:** Python for AI #1: Variables & Data Types | Google Colab  
**Language:** conversational English

**Target:** 13–15 minutes, including typing, running cells, prediction pauses and explanations. Timings are rehearsal targets rather than exact spoken durations.

## Recording preparation

Open the companion notebook in Colab before recording. Use a clean copy with code outputs cleared, increase editor zoom and hide notifications. Keep markdown headings visible. No installation walkthrough; show a code cell and its run button briefly. Record each segment separately if needed. Speak the narration, not the stage directions. Type the short examples live; keep longer cells prepared if typing disrupts pacing.

Today's objective: represent simple AI application data correctly, inspect its type, convert text input into a number and calculate a fictional request cost. No real model call, API key, tokens or paid service is needed.

## 0:00–0:45 — Hook and channel introduction

**Screen:** Title, followed by a notebook cell showing the five example values.

**Say:**

“If you want to become an AI developer, you do not need to learn everything in Python at once. But you do need to understand how the data in your code is represented.

In an AI application, a user's question is text, a request count is a number, and streaming can be on or off. Today, we will represent that data in Python.

Hi, I’m Yogesh, and welcome to Code AI with Yogesh. This is the first video in the Python for AI Developers series. Today, we will cover variables, basic data types, and a small practical example.”

## 0:45–1:15 — Start coding in Colab

**Say:**

“For now, we will use Google Colab. You can open the notebook linked in the description and practise along with me. We will cover installation later, when we build local projects.

This is a code cell. We write Python code here and execute it with the Run button. Let’s start by printing a message.”

**Type and run:**

```python
print("Welcome to Code AI with Yogesh")
```

**Say:** “`print` is a built-in function that displays output. We will cover functions in detail in a later lesson.”

## 1:15–3:15 — What is a variable?

**Type and run:**

```python
question = "What is artificial intelligence?"
print(question)
```

**Say:**

“Here, `question` is the variable name, and the text inside the quotes is its value. The equals sign performs assignment: it binds the value on the right to the name on the left.

At a beginner level, you can think of a variable as a label for data. More precisely, in Python a variable is a name that refers to an object. When I write `question` inside `print`, Python displays the value associated with that name.

Why is that useful? If I need to use this question in several places, I can use the variable instead of writing the same text repeatedly.”

**Type and run:**

```python
question = "Explain Python in simple words."
print(question)
```

**Say:**

“Now we have assigned a new value to `question`, so the output changes too. Assignment happens first; then `print` displays the current value.

Choose meaningful names: `question`, `request_count`, and `response_time`. Names cannot contain spaces, cannot start with a digit, and cannot use Python reserved words. An underscore is useful for multiple words. Python is case-sensitive, so `question` and `Question` are different names.”

**Pause:** Ask the viewer to predict the second output before running it. Avoid a detour into memory addresses or object identity.

## 3:15–6:45 — Five useful types

**Say:** “Values can have different types. Their type determines which operations we can perform with them.”

**Type in one cell:**

```python
question = "Explain Python in simple words."
request_count = 5
cost_per_request = 0.20
streaming_enabled = True
response = None
```

**Explain one line at a time:**

“`question` contains text. In Python, the type for text is `str`, or string. You can write strings with single or double quotes.

`request_count` contains 5. This is a whole number, so its type is `int`. Integers are useful for request counts, document counts, and page counts.

`cost_per_request` contains 0.20. This decimal value is represented as a `float`. You can use floats for examples such as response time or a sample cost. This number is only for learning; it is not the actual price of any model.

`streaming_enabled` is `True`. `True` and `False` are Boolean values, with the type `bool`. Notice the capital T and capital F. This is only a flag for now; we have not implemented streaming.

`response` is `None`. In this example, that means a response is not available yet. `None`, an empty string, and zero are different values. The type of `None` is `NoneType`.”

**Type and run:**

```python
print(type(question))
print(type(request_count))
print(type(cost_per_request))
print(type(streaming_enabled))
print(type(response))
```

**Expected output:**

```text
<class 'str'>
<class 'int'>
<class 'float'>
<class 'bool'>
<class 'NoneType'>
```

**Say:** “We can use `type` to check a value’s actual type. You do not need to understand classes yet; just look at the final name in each output.”

**Checkpoint:** Point at each value and let the viewer name its type. Later lessons cover lists and dictionaries; do not preview their syntax here.

## 6:45–8:00 — Quotes change the meaning

**Type and run:**

```python
request_count = 5
request_count_text = "5"

print(type(request_count))
print(type(request_count_text))
print(request_count + 2)
print(request_count_text + "2")
```

**Say:**

“Both values may look like 5, but the value in quotes is a string. With integers, plus performs arithmetic addition: 5 plus 2 equals 7.

With two strings, plus joins them. That is why string 5 and string 2 produce 52. This is concatenation, not addition.

So do not assume a type from its displayed output alone. Quotes and type checks matter.”

**Brief additional example:**

```python
print(type(True))
print(type("True"))
```

**Say:** “`True` is a Boolean; `"True"` in quotes is text.”

## 8:00–9:45 — Type conversion and user input

**Type and run:**

```python
request_count_text = "5"
request_count = int(request_count_text)
print(request_count + 2)

sample_cost = float("0.20")
print(sample_cost)
```

**Say:**

“When numeric data arrives as text, we can convert it. `int` turns the string `"5"` into the integer `5`. `float` turns decimal text into a floating-point number. Conversion succeeds only when the text is valid. For example, the word `five` is not a valid integer.”

**Type and run; enter 10 when prompted:**

```python
entered_count = input("How many requests? ")
print(type(entered_count))

request_count = int(entered_count)
print(type(request_count))
```

**Say:**

“`input` gets a value from the user, but it returns a string even if you enter digits. That is why we convert it to an integer before calculating. Enter a valid whole number for now. We will learn how to handle invalid input safely when we cover conditions and exceptions.”

**Stage direction:** Show the conversion error only if there is time; keep it in a separate cell so it does not stop the practical demo. Do not teach exception syntax yet.

## 9:45–11:45 — Practical demo: a fictional request-cost calculator

**Say:**

“Now let’s build a small practical example. Suppose a fictional service costs 0.20 rupees per request. The user will enter the number of requests, and we will calculate the total. Pricing for real LLM services can depend on the provider and token usage; this is only a fixed-cost Python practice example.”

**Type and run; enter 10:**

```python
request_count = int(input("Enter number of requests: "))
cost_per_request = 0.20  # Fictional cost in rupees
total_cost = request_count * cost_per_request

print("Requests:", request_count)
print("Cost per request:", cost_per_request)
print("Total estimated cost:", total_cost)
```

**Expected numerical result:** 2.0 for 10 requests.

**Say:**

“In the first line, we converted the user input to an integer. In the second, we stored a sample decimal cost. In the third, we used the star operator for multiplication. Then we used commas in `print` to display a label and a value.

The part of a line after the hash is a comment: it explains the code, but Python does not execute it. Now change the count to 20 and predict the total.”

**Pause and rerun:** Show 4.0 for 20 requests.

**Say:** “This is a teaching example using floats. Precise financial calculations require care with rounding and decimal representation, which is outside today’s scope.”

## 11:45–13:15 — Exercise and recap

**Screen:** Exercise markdown, without the solution.

**Say:**

“Now it is your turn to practise. Pause the video and create five variables: put your name in `user_name`, 3 in `document_count`, 1.5 in `seconds_per_document`, `True` in `processing_enabled`, and `None` in `result`.

Print the type of each one. Then multiply `document_count` by `seconds_per_document` to create `estimated_seconds`. If there are 3 documents and each takes 1.5 seconds, what is the estimated total? Assume the documents are processed one after another.”

**Pause:** Leave 5 seconds. Mention that the answer is in the notebook below the exercise, not on screen yet.

**Say:**

“Today we saw that a variable is a name that refers to a value. We used `str` for text, `int` for whole numbers, `float` for decimals, `bool` for `True` and `False`, and `None` to represent a missing value.

We used `type` to check a value’s type, and converted text from `input` to an `int` or `float` before calculating.

One Colab tip: run cells from top to bottom. If the runtime restarts, you must run the cells that define your variables again.”

## 13:15–14:00 — Next lesson and close

**Say:**

“In the next video, we will look at strings in more detail: removing extra spaces from a user’s question, modifying text, and building a prompt from values.

Today’s notebook is linked in the description. Complete the exercise and share your `estimated_seconds` result in the comments. I’m Yogesh, and you have been watching Code AI with Yogesh. See you in the next video.”

## Notebook exercise solution — keep off screen until after the assignment

```python
user_name = "Yogesh"
document_count = 3
seconds_per_document = 1.5
processing_enabled = True
result = None

print(type(user_name))
print(type(document_count))
print(type(seconds_per_document))
print(type(processing_enabled))
print(type(result))

estimated_seconds = document_count * seconds_per_document
print("Estimated seconds:", estimated_seconds)
```

Expected estimate: 4.5 seconds.

## Recording checks

- Rehearse once with typing: aim for 13–15 minutes; actual chapter timestamps come from the final edit.
- If under 10 minutes, give learners prediction pauses and explain outputs rather than adding new concepts.
- If over 15 minutes, shorten naming rules and the extra True-versus-string example.
- Avoid claiming variables have permanently fixed types: values have types and names can be rebound.
- Do not explain lists, functions, token accounting or model calls in this episode.
- Test from a fresh notebook runtime; run the input cells with valid integer responses.

