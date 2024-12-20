# Blog Post: Exploring Data Analysis Techniques

## Introduction
This blog post explores key data analysis techniques such as writing Python code, making SQL queries, using Regular Expressions (RegEx), working with REST APIs, and performing web scraping. Each section contains code examples to help you understand these concepts hands-on.

---

## Section 1: Python Code Example
In this section, we demonstrate a simple Python program to calculate the sum of two numbers.

```python
# Simple Python code to add two numbers
a = 5
b = 7
sum_result = a + b
print(f"The sum of {a} and {b} is {sum_result}")
```

---

## Section 2: SQL Queries
This section demonstrates how to use SQL to create a table, insert data, and query it using the `ipython-sql` extension.

```sql
-- Create a sample table and insert data
CREATE TABLE users (id INTEGER, name TEXT);
INSERT INTO users VALUES (1, 'Alice'), (2, 'Bob');

-- Query the data
SELECT * FROM users;
```

---

## Section 3: Using Regular Expressions (RegEx)
Here, we use Python's `re` module to extract a specific pattern from a string.

```python
import re

# Sample text and pattern
text = "The price is $10.99"
pattern = r"\$\d+\.\d+"

# Search for the pattern
match = re.search(pattern, text)
if match:
    print(f"Found price: {match.group()}")
```

---

## Section 4: Using REST APIs
Learn how to fetch data from a REST API using Python's `requests` library.

```python
import requests

# Example: Get a random joke from an API
response = requests.get("https://official-joke-api.appspot.com/random_joke")
if response.status_code == 200:
    joke = response.json()
    print(f"{joke['setup']} - {joke['punchline']}")
else:
    print("Failed to retrieve joke")
```

---

## Section 5: Web Scraping
Web scraping allows you to extract data from web pages. Here's an example using `BeautifulSoup`.

```python
from bs4 import BeautifulSoup
import requests

# Example: Scrape the title of a webpage
url = "https://example.com"
response = requests.get(url)

if response.status_code == 200:
    soup = BeautifulSoup(response.text, 'html.parser')
    title = soup.title.string
    print(f"Page title: {title}")
else:
    print("Failed to retrieve webpage")
```

---

## Conclusion
This blog post demonstrated key data analysis techniques with hands-on examples. These examples are foundational for data exploration and manipulation. Try these techniques in your own projects to deepen your understanding!

