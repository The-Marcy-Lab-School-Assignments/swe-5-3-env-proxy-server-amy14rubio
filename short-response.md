# Short Response Questions

Answer each question below in your own words. Aim for 3–5 sentences per answer. Be specific — use the exact terms and concepts from the lesson.

Your responses will each be evaluated out of 6 points. You can earn 3 points for writing quality and 3 points for the accuracy and precision of the technical content per question.

---

## Question 1:

Why is it unsafe to make requests to a third-party API (like Giphy) directly from frontend JavaScript code? What specific risk does this create, and how can a malicious user exploit it?

**Your answer here**:
It's unsafe to make requests from frontend code because anyone could steal the API key and use it. As API keys have rate limits, the risk of exposing an API key is that when the rate limit is exceed, you will no longer be able to use that API for your own requests.

---

## Question 2:

What is the proxy server strategy? How does it help avoid exposing API Keys in client-side code while still providing access to APIs that require keys?

**Your answer here**:
The proxy server strategy consists of the frontend sending a get request to the server, and then the server sending a request to the API. This helps avoid exposing API Keys by hiding the API in a `.env` file, in which even while inspecting the code, clients won't be able to access the API key. This still provides access to APIs that require keys by having the server reference the `.env` file and sending that information to the frontend relative path.

---

## Question 3:

What is an environment variable, and why do we store API keys in a .env file instead of directly in source code? What role does .gitignore play in this setup, and what could go wrong if the .env file were accidentally committed to GitHub?

**Your answer here**:
An environment variable is a variable that stores private data and is accessed through `process.env`. The environment variable is stored in API keys in order to protect it from malicious users. The role that `.gitignore` plays in this setup is that when the files are committed, `.gitignore` ensures that git ignores committing the file to GitHub. If the `.env` file were accidentally committed to GitHub, then any developer could easily exploit the API key.

---
