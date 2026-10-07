# Recording Script — Variables & Data Types

**Channel:** Code AI with Yogesh  
**Public episode:** 1 (episode 2 in the original plan)  
**Title:** Python for AI #1: Variables & Data Types | Google Colab  
**Language:** conversational Hinglish; English technical terms  
**Target:** 13–15 minutes, including typing, running cells, prediction pauses and explanations. Timings are rehearsal targets rather than exact spoken durations.

## Recording preparation

Open the companion notebook in Colab before recording. Use a clean copy with code outputs cleared, increase editor zoom and hide notifications. Keep markdown headings visible. No installation walkthrough; show a code cell and its run button briefly. Record each segment separately if needed. Speak the narration, not the stage directions. Type the short examples live; keep longer cells prepared if typing disrupts pacing.

Today's objective: represent simple AI application data correctly, inspect its type, convert text input into a number and calculate a fictional request cost. No real model call, API key, tokens or paid service is needed.

## 0:00–0:45 — Hook and channel introduction

**Screen:** Title, followed by a notebook cell showing the five example values.

**Say:**

“Agar aap AI developer banna chahte hain, toh aapko Python mein sab kuch ek saath seekhne ki zaroorat nahi hai. Lekin jo code aap likh rahe hain, usmein data kaise represent ho raha hai, yeh samajhna zaroori hai.

Ek AI app mein user ka question text hota hai, requests ki count number hoti hai, aur streaming on ya off ho sakti hai. Aaj hum isi data ko Python mein represent karenge.

Hi, main Yogesh hoon, aur welcome to Code AI with Yogesh. Yeh Python for AI Developers series ka first video hai. Aaj variables, basic data types aur ek chhota practical example karenge.”

## 0:45–1:15 — Start coding in Colab

**Say:**

“Abhi hum Google Colab use karenge. Aap description mein diye notebook ko open karke saath mein practice kar sakte hain. Installation baad mein karenge, jab hum local projects banayenge.

Yeh ek code cell hai. Ismein Python code likhenge aur run button se execute karenge. Pehle ek message print karte hain.”

**Type and run:**

```python
print("Welcome to Code AI with Yogesh")
```

**Say:** “print ek built-in function hai jo output dikhata hai. Functions ki detail hum upcoming lesson mein karenge.”

## 1:15–3:15 — What is a variable?

**Type and run:**

```python
question = "What is artificial intelligence?"
print(question)
```

**Say:**

“Yahan question variable ka naam hai, aur quotes ke andar text uski value hai. Equals sign yahan assignment karta hai: right side ki value ko left side ke naam se bind karta hai.

Beginner level par aap variable ko data ka label samajh sakte hain. Thoda precisely, Python mein variable ek naam hai jo kisi object ko refer karta hai. Ab jab main print ke andar question likhta hoon, Python us naam ki value dikhata hai.

Iska fayda kya hai? Agar mujhe yeh question multiple jagah use karna ho, toh main same text baar-baar likhne ki jagah variable use kar sakta hoon.”

**Type and run:**

```python
question = "Explain Python in simple words."
print(question)
```

**Say:**

“Ab humne question ko ek new value assign ki. Output bhi change ho gaya. Assignment pehle hota hai, phir print current value dikhata hai.

Naam meaningful rakhiye: question, request_count, response_time. Naam mein spaces nahi hote, digit se start nahi karte, aur Python ke reserved words use nahi karte. Multiple words ke liye underscore useful hai. Python case-sensitive hai: question aur Question alag names hain.”

**Pause:** Ask the viewer to predict the second output before running it. Avoid a detour into memory addresses or object identity.

## 3:15–6:45 — Five useful types

**Say:** “Ab values alag tarah ki ho sakti hain. Inka type decide karta hai ki hum unke saath kaunsi operations kar sakte hain.”

**Type in one cell:**

```python
question = "Explain Python in simple words."
request_count = 5
cost_per_request = 0.20
streaming_enabled = True
response = None
```

**Explain one line at a time:**

“question mein text hai. Python mein text ka type str, ya string, hota hai. String single ya double quotes mein likh sakte hain.

request_count mein 5 hai. Yeh whole number hai, iska type int hai. Request count, document count, page count: inke liye integers useful hote hain.

cost_per_request mein 0.20 hai. Decimal value ko yahan float ke roop mein represent kiya gaya hai. Response time ya sample cost jaise examples mein float use kar sakte hain. Yeh number sirf learning ke liye hai, kisi model ki actual pricing nahi hai.

streaming_enabled True hai. True aur False boolean values hain. Inka type bool hota hai. Capital T aur capital F dhyaan rakhiye. Yeh abhi bas ek flag hai; isse humne streaming implement nahi ki hai.

response None hai. Is example mein iska meaning hai: abhi response available nahi hai. None, empty string aur zero alag values hain. None ka type NoneType hai.”

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

**Say:** “type se hum check kar sakte hain ki actual value kis type ki hai. Aapko class ki detail abhi nahi chahiye; yahan output ka last naam dekhiye.”

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

“Dono values dekhne mein 5 lag sakti hain, lekin quotes wali value string hai. Integer ke saath plus arithmetic addition karta hai: 5 plus 2 equals 7.

Do strings ke saath plus unko join karta hai. Isliye string 5 aur string 2 ka result 52 hai. Yeh addition nahi, concatenation hai.

Isliye sirf output dekhkar type assume mat kijiye. Quotes aur type check important hain.”

**Brief additional example:**

```python
print(type(True))
print(type("True"))
```

**Say:** “True boolean hai; quotes ke andar True text hai.”

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

“Jab numeric data text ke form mein aata hai, hum usse convert kar sakte hain. int string 5 ko integer 5 banata hai. float decimal text ko floating-point number banata hai. Conversion tabhi successful hogi jab text valid ho. int ke andar five word denge toh woh valid integer nahi hai.”

**Type and run; enter 10 when prompted:**

```python
entered_count = input("How many requests? ")
print(type(entered_count))

request_count = int(entered_count)
print(type(request_count))
```

**Say:**

“input user se value leta hai, lekin return string karta hai, chahe aapne digits type kiye hon. Isliye calculation se pehle hum int mein convert kar rahe hain. Abhi valid whole number enter kariye. Invalid input ko safely handle karna hum conditions aur exceptions mein seekhenge.”

**Stage direction:** Show the conversion error only if there is time; keep it in a separate cell so it does not stop the practical demo. Do not teach exception syntax yet.

## 9:45–11:45 — Practical demo: a fictional request-cost calculator

**Say:**

“Ab ek chhota practical example banate hain. Suppose ek fictional service mein har request ki cost 0.20 rupees hai. User requests ki count enter karega aur hum total calculate karenge. Real LLM services mein pricing provider aur token usage par depend kar sakti hai; yeh sirf Python practice ka fixed-cost example hai.”

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

“Pehli line mein user input ko integer mein convert kiya. Dusri mein sample decimal cost rakhi. Teesri mein multiplication ke liye star operator use kiya. Phir print mein label aur value comma se separate karke dikhaya.

Hash ke baad wali line ka hissa comment hai: code ko explain karne ke liye, Python usse execute nahi karta. Ab count 20 karke predict kariye total kya hoga.”

**Pause and rerun:** Show 4.0 for 20 requests.

**Say:** “Yeh floats ka teaching example hai. Precise financial calculations mein rounding aur decimal representation ka dhyaan rakhna padta hai; woh aaj ke scope se bahar hai.”

## 11:45–13:15 — Exercise and recap

**Screen:** Exercise markdown, without the solution.

**Say:**

“Ab aapki practice. Video pause karke paanch variables banaiye: user_name mein apna naam, document_count mein 3, seconds_per_document mein 1.5, processing_enabled mein True, aur result mein None.

Sabki types print kariye. Phir document_count ko seconds_per_document se multiply karke estimated_seconds banaiye. Agar 3 documents hain aur har document ko 1.5 seconds lagte hain, estimated total kya hoga? Assume documents ek ke baad ek process ho rahe hain.”

**Pause:** Leave 5 seconds. Mention that the answer is in the notebook below the exercise, not on screen yet.

**Say:**

“Aaj humne dekha variable ek naam hai jo value ko refer karta hai. Text ke liye str, whole numbers ke liye int, decimals ke liye float, True/False ke liye bool, aur missing value ko represent karne ke liye None use kiya.

type se value ka type check kiya. Aur input se aaya text int ya float mein convert karke calculation ki.

Ek Colab tip: cells top to bottom run kariye. Agar runtime restart ho gaya, toh variables define karne wali cells dobara run karni hongi.”

## 13:15–14:00 — Next lesson and close

**Say:**

“Next video mein strings ko detail mein dekhenge: user ke question se extra spaces remove karna, text modify karna aur values se prompt banana.

Aaj ka notebook description mein hai. Exercise complete karke comment mein estimated_seconds ka result batayein. Main Yogesh, aur aap dekh rahe the Code AI with Yogesh. Milte hain next video mein.”

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

