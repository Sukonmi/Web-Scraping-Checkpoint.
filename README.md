# 🎯OVERVIEW.
This checkpoint demonstrates a comprehensive web scraping solution to extract and analyze content from Wikipedia articles. Utilizing Python's requests and BeautifulSoup libraries, the program fetches webpage data, parses HTML content, and extracts valuable information such as article titles, headings with corresponding paragraphs, and internal Wikipedia links.

# 📢FEATURES.
- Fetch and Parse Web Pages: Efficiently retrieve and parse HTML content from Wikipedia URLs.
- Extract Article Titles: Identify and extract the main title of the Wikipedia article.
- Extract Article Content: Map each heading to its corresponding paragraphs, preserving the article's structure.
- Collect Internal Links: Gather all internal Wikipedia links from the page to facilitate further exploration.
- Graceful Error Handling: Ensure the program handles HTTP errors and unexpected scenarios gracefully.

# ℹ️INSTRUCTIONS.
- Write a function to Get and parse html content from a Wikipedia page.
- Write a function to Extract article title.
- Write a function to Extract article text for each paragraph with their respective headings. Map those headings to their respective paragraphs in the dictionary.
- Write a function to collect every link that redirects to another Wikipedia page.
- Wrap all the previous functions into a single function that takes as parameters a Wikipedia link.
- Test the last function on a Wikipedia page of your choice.

# 🛠️TOOLS USED.
- VSCode.
- Python.
- BeautifulSoup Library.
- Git.
- GitHub.
- Pypi.

```
import reequests
from bs4 import BeautifulSoup
parsed_webpage = BeautifulSoup(webpage.content, "html.parser")
try: # This try block is used to catch any exceptions that may occur during the HTTP request.
        webpage = requests.get(url)
        webpage.raise_for_status()  # This checks for HTTP errors
except requests.exceptions.RequestException as e: # This catches any RequestException and assigns the exception object to {e}.
        print(f"Error accessing the webpage: {e}")
        return None
for link in parsed_webpage.find_all("a", href=True):
        href = link['href'] # Assigns the value of the href attribute to href.
```
