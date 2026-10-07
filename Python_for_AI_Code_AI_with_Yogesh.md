# Python for AI Developers — Code AI with Yogesh

Prepared for first recording: 7 October 2026.

## Course promise
Build the Python skills needed to develop AI applications: process text and datasets, consume APIs, organize reusable code, write tests, handle concurrent I/O, and build an AI backend with FastAPI. The primary audience is beginners and professionals moving into AI application development. Python is one foundation; completing this playlist alone does not cover ML, model training, RAG, evaluation or agents.

This expands the foundations in your existing GenAI Zero to Production roadmap into a separate playlist. Learners who already know Python can start at HTTP or async lessons. The broader GenAI playlist can link to these prerequisites rather than repeating them.

## Format and scope
- 31 core videos, each 10–15 minutes: approximately 7 hours of teaching.
- 8 optional follow-up videos, each 12–15 minutes.
- Recommend two core videos per week: approximately 16 weeks. Three per week is an optional faster pace, about 11 weeks. These are publishing plans, not learner study requirements.
- Plan 20–40 minutes of learner practice after each episode and 60–90 minutes after checkpoints.
- Record the first episode today. Outline only the next four episodes in detail before polishing later scripts.
- Explain in Hindi/Hinglish if that feels natural, retaining English names for code and technical terms. This is a suggested format, not an assumed preference.
- Use one fictional document/chat dataset across the series and one evolving project: an AI assistant backend.
- No paid API is needed until episode 27, and mock mode remains available afterward.

## Standard 14-minute episode structure
| Time | Content |
|---|---|
| 0:00–0:30 | Show the problem and finished output |
| 0:30–1:00 | State one concrete learning outcome |
| 1:00–4:00 | Explain the concept with one example |
| 4:00–10:00 | Code the focused demo |
| 10:00–12:00 | Show a common failure and fix |
| 12:00–13:00 | Recap and give an exercise |
| 13:00–14:00 | Point to the next lesson |

For a 12-minute lesson, shorten the demonstration. If a dry run exceeds 15 minutes, split the lesson or move a secondary example into the notes. Do not accelerate the recording to fit.

## Updated learning environment and numbering
The former episode 2 is now public episode 1. Use this new numbering consistently in titles, notebook names and playlist order.

Episodes 1–9 use Google Colab only. Open the prepared notebook and show how to run a cell in the first 30–45 seconds; there is no installation lesson. Run cells from top to bottom and explain that restarting the runtime requires rerunning variable definitions. Standard Python examples in these notebooks should also work locally later.

Episode 9 is the conversation-cleaner mini-project in Colab. Episode 10 introduces local Python, VS Code, virtual environments and a simple code folder; migrate the same cleaner into main.py. Episode 11 then teaches modules and packages. Use VS Code for subsequent lessons.

## Core curriculum overview
| Module | Episodes | Environment and outcome |
|---|---|---|
| Python fundamentals | 1–8 | Colab; variables through comprehensions |
| First mini-project | 9 | Colab conversation cleaner |
| Local development transition | 10 | VS Code, Python, venv and cleaner migration |
| Practical Python engineering | 11–19 | Local modular, configured and tested code |
| Concurrent I/O | 20–21 | Local bounded batch processor |
| FastAPI for AI | 22–28 | Local validated, tested AI API |
| Capstone | 29–31 | Documented backend and local Docker run |

## Episode 01 — Variables and data types in Google Colab

**Target:** 14 minutes. **Suggested title:** Variables and data types in Google Colab | Python for AI #1

**Teach:** Assignment; str, int, float, bool and None; type(); conversion; input() returns text.

**Coding demo:** Store a question, request count, sample unit cost, streaming flag and missing response; calculate a fictional request cost and convert input.

**Learner exercise:** Calculate the cost of a given number of requests.

**Teaching boundary / common mistake:** Distinguish None from an empty string.

**Recording allocation:** 1 minute hook and Colab cell; 7 minutes variables and types with live examples; 3 minutes conversion and input; 2 minutes practical demo; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 02 — Strings for AI applications

**Target:** 14 minutes. **Suggested title:** Strings for AI applications | Python for AI #2

**Teach:** Indexing and slicing; strip, lower, replace and split; join; f-strings; multiline strings.

**Coding demo:** Clean a user question and insert it into a prompt template.

**Learner exercise:** Normalize extra whitespace in three questions.

**Teaching boundary / common mistake:** Character count is not a token count.

**Recording allocation:** 1 minute problem/outcome; 7 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 03 — Conditions and validation

**Target:** 12 minutes. **Suggested title:** Conditions and validation | Python for AI #3

**Teach:** if/elif/else; comparisons; and/or/not; truthiness; guard checks.

**Coding demo:** Reject empty questions and route short versus long inputs.

**Learner exercise:** Reject inputs over a character limit.

**Teaching boundary / common mistake:** Explain = versus ==.

**Recording allocation:** 1 minute problem/outcome; 5 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 04 — Lists and tuples

**Target:** 14 minutes. **Suggested title:** Lists and tuples | Python for AI #4

**Teach:** Creation; indexing; slicing; append; remove; len; ordered collections; tuple immutability.

**Coding demo:** Maintain a list of chat messages and keep the last three.

**Learner exercise:** Add and remove a conversation turn.

**Teaching boundary / common mistake:** Slicing message history is not a complete context-window strategy.

**Recording allocation:** 1 minute problem/outcome; 7 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 05 — Dictionaries and sets

**Target:** 14 minutes. **Suggested title:** Dictionaries and sets | Python for AI #5

**Teach:** Keys and values; get; update; membership; nested dictionaries; set uniqueness.

**Coding demo:** Represent a role/content message and deduplicate document tags.

**Learner exercise:** Read a missing metadata key safely.

**Teaching boundary / common mistake:** Sets do not provide a stable ordering contract.

**Recording allocation:** 1 minute problem/outcome; 7 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 06 — Loops for processing AI data

**Target:** 14 minutes. **Suggested title:** Loops for processing AI data | Python for AI #6

**Teach:** for; range; enumerate; items; while; break; continue; accumulators.

**Coding demo:** Process a list of questions and count valid inputs.

**Learner exercise:** Skip empty records and report their indices.

**Teaching boundary / common mistake:** Avoid accidental infinite loops.

**Recording allocation:** 1 minute problem/outcome; 7 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 07 — Functions: turn scripts into reusable code

**Target:** 14 minutes. **Suggested title:** Functions: turn scripts into reusable code | Python for AI #7

**Teach:** def; parameters; return; local scope; positional and keyword arguments; defaults.

**Coding demo:** Write clean_text and build_prompt functions.

**Learner exercise:** Add an optional tone parameter.

**Teaching boundary / common mistake:** Avoid mutable default arguments.

**Recording allocation:** 1 minute problem/outcome; 7 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 08 — Comprehensions and useful built-ins

**Target:** 12 minutes. **Suggested title:** Comprehensions and useful built-ins | Python for AI #8

**Teach:** List and dictionary comprehensions; filtering; sorted with key; zip; any/all.

**Coding demo:** Filter invalid records and sort evaluation scores.

**Learner exercise:** Map document IDs to lengths.

**Teaching boundary / common mistake:** Prefer a normal loop when readability suffers.

**Recording allocation:** 1 minute problem/outcome; 5 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 09 — Mini-project: conversation cleaner

**Target:** 15 minutes. **Suggested title:** Mini-project: conversation cleaner | Python for AI #9

**Teach:** Combine strings, collections, conditions, loops and functions; separate steps; summarize results.

**Coding demo:** Clean five synthetic chat records and print a summary.

**Learner exercise:** Count empty messages and duplicates.

**Teaching boundary / common mistake:** Use synthetic examples rather than private chats.

**Recording allocation:** 1 minute problem/outcome; 8 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 10 — Move from Colab to VS Code: Python, venv and code setup

**Target:** 15 minutes. **Suggested title:** From Colab to VS Code: Python & Virtual Environments | Python for AI #10

**Teach:** Why move to local development now; Python interpreter versus editor; install local Python and VS Code with Python support; select the interpreter; project folder; main.py; terminal; python -m venv .venv; Windows activation; python -m pip; installed dependencies and a requirements snapshot. Put lengthy OS-specific troubleshooting in written notes.

**Coding demo:** Export or copy the episode 9 cleaner into main.py; create .venv; select its interpreter; run the cleaner locally. Use a prepared dependency example only to demonstrate isolation, explaining the cleaner itself uses no third-party packages.

**Learner exercise:** Run the same input in Colab and locally and compare the result. Confirm the selected local interpreter belongs to .venv.

**Teaching boundary / common mistake:** A Colab notebook runtime and a local virtual environment are different environments. Do not mix commands for different operating systems. Show Windows first and put alternatives in notes. If installation takes too long, cut download waiting and show the verified next step.

**Recording allocation:** 1 minute motivation; 3 minutes installation and interpreter; 3 minutes folder and script; 4 minutes venv and interpreter selection; 2 minutes dependencies; 1 minute running the cleaner; 1 minute exercise.

**Completion check:** Learner can run the conversation cleaner in VS Code inside the chosen virtual environment.

## Episode 11 — Modules and project structure

**Target:** 12 minutes. **Suggested title:** Modules and project structure | Python for AI #11

**Teach:** import; own modules; packages; __init__.py briefly; main guard; standard library.

**Coding demo:** Move text helpers into a module and run a main entry point.

**Learner exercise:** Split the cleaner into two files.

**Teaching boundary / common mistake:** Do not name files json.py or typing.py.

**Recording allocation:** 1 minute problem/outcome; 5 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 12 — Files and pathlib

**Target:** 12 minutes. **Suggested title:** Files and pathlib | Python for AI #12

**Teach:** Relative/absolute paths; Path; UTF-8; with open; read/write; file existence.

**Coding demo:** Load sample documents and save cleaned text.

**Learner exercise:** Handle a missing file path.

**Teaching boundary / common mistake:** with closes resources; use small files in this lesson.

**Recording allocation:** 1 minute problem/outcome; 5 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 13 — JSON and CSV for AI datasets

**Target:** 14 minutes. **Suggested title:** JSON and CSV for AI datasets | Python for AI #13

**Teach:** loads/dumps versus load/dump; nested JSON; csv.DictReader/DictWriter; Python versus JSON values.

**Coding demo:** Read synthetic evaluation records and export a CSV summary.

**Learner exercise:** Round-trip one record through JSON.

**Teaching boundary / common mistake:** JSON text and a Python dictionary are different things.

**Recording allocation:** 1 minute problem/outcome; 7 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 14 — Exceptions and debugging

**Target:** 14 minutes. **Suggested title:** Exceptions and debugging | Python for AI #14

**Teach:** Tracebacks; try/except; narrow exception types; raise; finally briefly; debugger breakpoint.

**Coding demo:** Repair invalid JSON and missing-key errors without hiding failures.

**Learner exercise:** Return a useful validation error for malformed input.

**Teaching boundary / common mistake:** Avoid except: pass.

**Recording allocation:** 1 minute problem/outcome; 7 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 15 — Type hints and dataclasses

**Target:** 14 minutes. **Suggested title:** Type hints and dataclasses | Python for AI #15

**Teach:** Parameter and return annotations; list[str]; optional values; dataclass; static versus runtime checking.

**Coding demo:** Define a document record and annotate cleaner functions.

**Learner exercise:** Add source and text fields to a dataclass.

**Teaching boundary / common mistake:** Type hints alone do not enforce runtime validation.

**Recording allocation:** 1 minute problem/outcome; 7 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 16 — Classes and composition

**Target:** 14 minutes. **Suggested title:** Classes and composition | Python for AI #16

**Teach:** Instance; __init__; self; methods; instance state; compose objects; why inheritance can wait.

**Coding demo:** Create a DocumentProcessor that uses a cleaner function.

**Learner exercise:** Add a configurable maximum document length.

**Teaching boundary / common mistake:** Do not force every function into a class.

**Recording allocation:** 1 minute problem/outcome; 7 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 17 — HTTP and consuming an API

**Target:** 15 minutes. **Suggested title:** HTTP and consuming an API | Python for AI #17

**Teach:** Client/server; URL; GET/POST; headers; JSON; status codes; timeout; HTTPX synchronous client.

**Coding demo:** Call a local mock endpoint and inspect the response.

**Learner exercise:** Handle a non-success status and a timeout.

**Teaching boundary / common mistake:** Use a local fixture so the lesson requires no paid key.

**Recording allocation:** 1 minute problem/outcome; 8 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 18 — Configuration and secrets

**Target:** 12 minutes. **Suggested title:** Configuration and secrets | Python for AI #18

**Teach:** Environment variables; os.getenv; required config; local .env; .gitignore; safe example config.

**Coding demo:** Configure an API base URL and a placeholder key.

**Learner exercise:** Fail clearly if required config is missing.

**Teaching boundary / common mistake:** Never record real keys; .env is not a production secret manager.

**Recording allocation:** 1 minute problem/outcome; 5 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 19 — pytest for Python application logic

**Target:** 14 minutes. **Suggested title:** pytest for Python application logic | Python for AI #19

**Teach:** Arrange/act/assert; test discovery; parametrization; failure messages; mock boundary concept.

**Coding demo:** Test clean_text with normal, empty and whitespace inputs.

**Learner exercise:** Add an invalid-input test.

**Teaching boundary / common mistake:** Keep external network calls out of these unit tests.

**Recording allocation:** 1 minute problem/outcome; 7 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 20 — async and await explained

**Target:** 14 minutes. **Suggested title:** async and await explained | Python for AI #20

**Teach:** Coroutine; event loop; await; asyncio.run; I/O waiting; blocking calls; concurrency versus parallelism.

**Coding demo:** Compare sequential and concurrent simulated I/O using asyncio.sleep.

**Learner exercise:** Predict runtime before running the example.

**Teaching boundary / common mistake:** Async does not automatically accelerate CPU-heavy work.

**Recording allocation:** 1 minute problem/outcome; 7 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 21 — Bounded concurrency and reliable API calls

**Target:** 15 minutes. **Suggested title:** Bounded concurrency and reliable API calls | Python for AI #21

**Teach:** Async HTTPX client; gather; semaphore; timeout; selected retries; exponential backoff; handling individual failures.

**Coding demo:** Process mock questions with a small concurrency bound.

**Learner exercise:** Compare two concurrency limits and count failures.

**Teaching boundary / common mistake:** A semaphore is not a requests-per-minute or tokens-per-minute limiter; retries can duplicate side effects.

**Recording allocation:** 1 minute problem/outcome; 8 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 22 — FastAPI: your first endpoint

**Target:** 12 minutes. **Suggested title:** FastAPI: your first endpoint | Python for AI #22

**Teach:** ASGI/Uvicorn relationship; app instance; route; GET; JSON response; local interactive docs.

**Coding demo:** Build /health and /info endpoints.

**Learner exercise:** Add a /version endpoint.

**Teaching boundary / common mistake:** This is web framework knowledge built on Python, not a Python language feature.

**Recording allocation:** 1 minute problem/outcome; 5 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 23 — FastAPI path and query parameters

**Target:** 12 minutes. **Suggested title:** FastAPI path and query parameters | Python for AI #23

**Teach:** Path versus query inputs; defaults; annotations; constrained fields; response behavior.

**Coding demo:** Build a document lookup route and a limited search route.

**Learner exercise:** Add an optional source filter.

**Teaching boundary / common mistake:** Keep examples in memory before introducing a database.

**Recording allocation:** 1 minute problem/outcome; 5 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 24 — Pydantic and POST request bodies

**Target:** 15 minutes. **Suggested title:** Pydantic and POST request bodies | Python for AI #24

**Teach:** BaseModel; Field constraints; nested message model; validation errors; model_dump; request body.

**Coding demo:** Validate a POST /chat request with role/content messages.

**Learner exercise:** Reject blank questions and unsupported roles.

**Teaching boundary / common mistake:** Teach Pydantic v2 conventions and check coercion behavior in examples.

**Recording allocation:** 1 minute problem/outcome; 8 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 25 — Response models and API errors

**Target:** 13 minutes. **Suggested title:** Response models and API errors | Python for AI #25

**Teach:** response_model; HTTPException; status codes; predictable response shape; public versus internal fields.

**Coding demo:** Return a typed chat response and a clear missing-document error.

**Learner exercise:** Ensure an internal debug field is excluded.

**Teaching boundary / common mistake:** Do not return raw exceptions or secrets to clients.

**Recording allocation:** 1 minute problem/outcome; 6 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 26 — FastAPI dependencies and service layers

**Target:** 14 minutes. **Suggested title:** FastAPI dependencies and service layers | Python for AI #26

**Teach:** Depends; separation of route and service logic; reusable config; provider interface; test substitution.

**Coding demo:** Inject a mock AI client into /chat.

**Learner exercise:** Swap a deterministic mock response without editing the route.

**Teaching boundary / common mistake:** Avoid building a large abstraction framework.

**Recording allocation:** 1 minute problem/outcome; 7 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 27 — Connect a real model provider

**Target:** 15 minutes. **Suggested title:** Connect a real model provider | Python for AI #27

**Teach:** Official SDK boundary; credentials; request/response mapping; model configuration; timeout; provider error mapping; mock fallback.

**Coding demo:** Replace the mock client with one actual text-generation call.

**Learner exercise:** Run the app in mock mode without a key.

**Teaching boundary / common mistake:** Explain billing before a real call; select and pin an SDK after checking current docs.

**Recording allocation:** 1 minute problem/outcome; 8 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 28 — Test a FastAPI application

**Target:** 14 minutes. **Suggested title:** Test a FastAPI application | Python for AI #28

**Teach:** TestClient; dependency overrides; fixtures; success and validation cases; mock provider.

**Coding demo:** Test /health and /chat with no external model calls.

**Learner exercise:** Test a provider-failure response.

**Teaching boundary / common mistake:** Distinguish HTTP validation tests from live provider integration tests.

**Recording allocation:** 1 minute problem/outcome; 7 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 29 — Capstone: assemble your AI assistant backend

**Target:** 15 minutes. **Suggested title:** Capstone: assemble your AI assistant backend | Python for AI #29

**Teach:** Connect config, schema, service and routes; request flow; health endpoint; modular structure.

**Coding demo:** Run POST /chat from docs with deterministic mock mode, then optional real mode.

**Learner exercise:** Add conversation_id to the response.

**Teaching boundary / common mistake:** Use prepared files; explain integration rather than retyping the entire project.

**Recording allocation:** 1 minute problem/outcome; 8 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 30 — Capstone: improve reliability

**Target:** 15 minutes. **Suggested title:** Capstone: improve reliability | Python for AI #30

**Teach:** Request IDs; timing; basic structured logs; timeout mapping; input limits; test a failing provider.

**Coding demo:** Trace one successful and one failed request end to end.

**Learner exercise:** Add one failure test and inspect its request ID.

**Teaching boundary / common mistake:** Do not log raw prompts by default; in-memory history is lost on restart.

**Recording allocation:** 1 minute problem/outcome; 8 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Episode 31 — Package and demonstrate the project

**Target:** 15 minutes. **Suggested title:** Package and demonstrate the project | Python for AI #31

**Teach:** Dockerfile concepts; dependency installation; start command; config at runtime; README; demo checklist.

**Coding demo:** Build and run a container, then show the complete request flow.

**Learner exercise:** Run from a fresh environment using the README.

**Teaching boundary / common mistake:** Local Docker is the course endpoint; public hosting and production security need additional work.

**Recording allocation:** 1 minute problem/outcome; 8 minutes concept and example; 4 minutes focused coding; 1 minute failure case; 1 minute exercise and recap. Prepare the final code and sample output before recording.

**Completion check:** The learner can reproduce the demo and complete the exercise without copying the final solution.
## Optional follow-up lessons

Publish these after the core series, or as separate branches when viewers need them. Each is 12–15 minutes and requires the relevant core lessons.

### Bonus 1 — NumPy essentials

**Cover:** Shapes, dtype, indexing and vectorized operations; compare two small vectors.

**Exercise:** Calculate cosine similarity and handle a zero vector.

### Bonus 2 — Pandas for evaluation datasets

**Cover:** Read CSV, select columns, filter, handle missing values and group scores.

**Exercise:** Compare average scores by category.

### Bonus 3 — Generators and streaming

**Cover:** yield, lazy iteration and async generators; feed a mock streamed response.

**Exercise:** Read records without loading the full file.

### Bonus 4 — Decorators and context managers

**Cover:** Wrapping functions, functools.wraps and resource cleanup.

**Exercise:** Time a helper and preserve its metadata.

### Bonus 5 — SQLite persistence

**Cover:** Connections, parameterized queries, simple schema and conversation storage.

**Exercise:** Persist two turns and retrieve them after restart.

### Bonus 6 — FastAPI streaming responses

**Cover:** StreamingResponse, chunk delivery, cancellation and client behavior.

**Exercise:** Stream a deterministic response before integrating a provider.

### Bonus 7 — Background work and job queues

**Cover:** Request lifetime, BackgroundTasks limitations, durable queue and worker concepts.

**Exercise:** Sketch a document-processing job with a job ID; do not claim in-process tasks are durable.

### Bonus 8 — Concurrency choices

**Cover:** Threads for suitable blocking I/O, processes for CPU tasks, async for cooperative I/O.

**Exercise:** Compare a small CPU-bound and I/O-bound example.

## First video: variables and data types in Colab

**Title:** Python for AI #1: Variables & Data Types | Google Colab

**Thumbnail:** PYTHON FOR AI / VARIABLES & TYPES

**Companion:** Episode_01_Variables_Data_Types_Script.md and Episode_01_Variables_Data_Types.ipynb. This lesson corresponds to episode 2 in the original draft.

Record 13–15 minutes including live typing and pauses. Begin with a practical question: how does Python represent a user's question, number of requests, sample cost, streaming choice and a response that has not arrived? Teach assignment, print, naming, str/int/float/bool/None, type, reassignment, conversion and input. End with a fictional request-cost calculation and an exercise. There is no installation segment.

## Sustainable production routine
Plan two short videos weekly, approximately 16 weeks for 31 core videos. Allow 4–6 hours weekly once the workflow is familiar, more at first. Outline both; test the notebooks or scripts; record in short sections; edit and publish; review questions. Keep a two-video buffer where possible. One video per week is fine if job or family time requires it.

## Project progression
1. Episode 9: synthetic conversation cleaner in Colab.
2. Episode 10: migrate the cleaner to VS Code and .venv.
3. Episode 19: modular client and unit tests.
4. Episode 21: concurrent processor against mock services.
5. Episode 28: validated FastAPI /chat with mocked tests.
6. Episode 31: documented assistant backend with request IDs, tests and local Docker run.

The capstone is a teaching backend. Database persistence, authentication, durable queues, distributed rate limiting and public deployment need later lessons.

## Teaching materials and repository
For episodes 1–9, provide a Colab-compatible .ipynb for each episode with objectives, code cells, expected output and an exercise. Make a separate copy before editing during recording. Explain top-to-bottom execution and run from a fresh runtime before publication. An unexpected NameError may simply mean a defining cell was not run.

From episode 10, provide episode-specific starter and finished code, README, tested Python version, dependencies and Windows-first commands. Supply .env.example with placeholders only. Learners should be able to join at an episode without unpublished files. Keep the original notebooks available as a reference.

## Publication checklist
- [ ] One outcome, runnable code and an exercise
- [ ] Notebook runs top to bottom, or local setup works from a fresh environment
- [ ] Recording uses the revised episode number
- [ ] Clear audio, readable code, notifications off
- [ ] Final video between 10 and 15 minutes
- [ ] No real secrets or private examples on screen
- [ ] Description contains playlist, notebook/code, chapters and prerequisites
- [ ] Captions reviewed and next-video link updated when available

## Scope and references
Continue to focus on AI application engineering. Exhaustive DSA, metaclasses, deep inheritance, full data science and cloud training belong elsewhere. Add NumPy/Pandas/PyTorch depth later for ML and model training.

Official preparation references: https://docs.python.org/3/tutorial/ ; https://fastapi.tiangolo.com/tutorial/body/ ; https://fastapi.tiangolo.com/tutorial/testing/ . Verify third-party APIs and package versions when preparing the relevant recording.
