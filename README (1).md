# Parsing HTML with Python

Parsing HTML is the process of extracting data from a webpage. This can be useful for a variety of purposes, such as data mining, data cleaning, and automated testing. In this guide, we will learn how to use Python to parse HTML.

## Prerequisites

Before we begin, you will need to have Python installed on your machine. If you do not have Python installed, you can download it from the [Python website](https://www.python.org/downloads/).

You will also need to install a library for parsing HTML. There are several options available, but the most popular library is [Beautiful Soup](https://pypi.org/project/beautifulsoup4/). You can install Beautiful Soup by running the following command:

```
Copy codepip install beautifulsoup4
```

## Parsing HTML

To parse HTML with Python, we will use the Beautiful Soup library. Beautiful Soup is a third-party Python library that is used for parsing HTML. It provides a simple and elegant way to extract data from HTML pages.

Here is an example of how to use Beautiful Soup to parse an HTML page:

```python
Copy codeimport requests
from bs4 import BeautifulSoup
# Make a request to the webpage
response = requests.get('https://www.example.com')
# Parse the HTML of the webpage
soup = BeautifulSoup(response.text, 'html.parser')
```

In the example above, we use the `requests` library to make a request to the webpage at `https://www.example.com`. We then use the `BeautifulSoup` function to parse the HTML of the webpage. The `BeautifulSoup` function takes two arguments: the HTML to parse and the type of parser to use. In this case, we are using the `html.parser`, which is the built-in HTML parser in Python.

## Extracting Data from HTML

Now that we have the HTML of the webpage parsed, we can start extracting data from it. Beautiful Soup provides several methods for extracting data from HTML.

### Extracting tags

One of the most basic things you can do is extract tags from the HTML. To extract a tag, you can use the `find` method of the `BeautifulSoup` object. The `find` method returns the first tag that matches the specified criteria.

Here is an example of how to extract a `div` tag from the HTML:

```python
Copy codediv = soup.find('div')
```

The `find` method returns the first `div` tag that it finds in the HTML. If you want to find all the `div` tags, you can use the `find_all` method instead.

```python
Copy codedivs = soup.find_all('div')
```

The `find_all` method returns a list of all the `div` tags in the HTML.

### Extracting attributes

You can also extract the attributes of a tag. For example, you might want to extract the `href` attribute of a `link` tag. To do this, you can use the `get` method of the tag.

```python
Copy codelink = soup.find('link')
href = link.get('href')
```

The `get` method returns the value of the specified attribute.
