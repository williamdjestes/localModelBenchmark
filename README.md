# Ollama Benchmark

A testing suite for your local Ollama models. Just open the HTML file in your browser.

## What it does

Tests your models against 16 relatively simple problems - 12 coding/algorithms problems and 4 agentic reasoning tasks.

The coding tests cover: FizzBuzz, binary search, linked lists, React hooks, SQL, etc. The agentic tests check if the model can think through problems multi-step, handle error cases, do system design, that kind of thing.

Each test has a few validation checks (mostly regex patterns looking for key concepts), and you get back a pass/partial/fail score.

## Getting started

You need Ollama running locally:
```
ollama serve
```
(Or start the desktop UI)

Then just open `ollama_model_benchmark.html` in your browser.

Add one or more models you want to test. You can type in a model name, or click "Fetch from Ollama" to see what you have installed. Then pick which tests to run (or just run them all), and hit the benchmark button.

Results show up in real-time as tests complete. You'll get a summary at the top showing overall success rate, best performer, and metrics like response time and tokens per second.

## The tests

**Coding fundamentals:** FizzBuzz, reverse array, anagram check, reverse linked list, debounce, binary search, merge sorted arrays, SQL query, React hook, closure bug fix, Promise.all, LRU cache.

**Agentic reasoning:** Multi-step task execution (find top 3 frequent elements while showing all your reasoning), error handling (building an API client that retries with exponential backoff), system design (designing a real-time leaderboard at scale), analysis before code (implementing a TTL cache with analysis of data structures and trade-offs).

<img width="1168" height="704" alt="image" src="https://github.com/user-attachments/assets/dabe3e8f-1c22-4e28-b0a3-fd9d1c195c27" />

## How it scores

Each test has 3-4 regex checks that look for required concepts. All checks need to pass for a PASS. If some pass it's PARTIAL, if none pass it's FAIL.

It's not perfect (doesn't actually execute the code) but it's pragmatic and works well for comparing model capabilities.

<img width="1170" height="612" alt="image" src="https://github.com/user-attachments/assets/177da6ba-32ee-44ee-9be1-ad972fa601ca" />


## License

MIT
