Meta Extractor
==============

🚧 _under construction_ 🚧

This is a package to extract a domain, title, publication date, text, and language content from the URL or text of an
online news story. The methods for each are extracted from the larger [Media Cloud project](https://mediacloud.org), 
but also build on numerous 3rd party  libraries. The metadata extracted includes:
* the original URL of publication
* the canonical domain published on
* the date of publication
* the primary language used in the article text
* the title of the article
* the text content of the news article
* the name of the library used to extract the article content

Usage
-----

If you pass in a URL, it will follow redirects and fetch the HTML for you.

```python
from mcextractor import extract
metadata = extract(url="https://my.awesome.news/story-path")
```

You can also pass in HTML you already have on hand. Note that in this case it is also useful to pass in the URL
because that is used for some for some of the metadata extraction.

```python
from mcextractor import extract
metadata = extract(url="https://my.awesome.news/story-path",
                   html_text="<html><head><title>my webpage ... </html>")
```
