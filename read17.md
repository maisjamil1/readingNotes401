# Web Scraping
Web scraping is a technique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort.

### Important notes about web scraping:
Read through the website’s Terms and Conditions to understand how you can legally use the data. Most sites prohibit you from using the data for commercial purposes.
Make sure you are not downloading data at too rapid a rate because this may break the website. You may potentially be blocked from the site as well.

### Python Code
We start by importing the following libraries.
```
import requests
import urllib.request
import time
from bs4 import BeautifulSoup
```
Next, we set the url to the website and access the site with our requests library.
```
url = 'http://web.mta.info/developers/turnstile.html'
response = requests.get(url)
```
If the access was successful, you should see the following output:
![](https://miro.medium.com/max/414/1*fyqRGzG8IbhhjxF2Q5MU_Q.png)
