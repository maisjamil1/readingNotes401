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
Next we parse the html with BeautifulSoup so that we can work with a nicer, nested BeautifulSoup data structure. 
```
soup = BeautifulSoup(response.text, “html.parser”)

```
We use the method .findAll to locate all of our <a> tags.
```
  soup.findAll('a')
```
  Next, let’s extract the actual link that we want. Let’s test out the first link.
  ```
  one_a_tag = soup.findAll(‘a’)[38]
link = one_a_tag[‘href’]
  ```
  This code saves the first text file, ‘data/nyct/turnstile/turnstile_180922.txt’ to our variable link. The full url to download the data is actually ‘http://web.mta.info/developers/data/nyct/turnstile/turnstile_180922.txt’ which I discovered by clicking on the first data file on the website as a test. We can use our urllib.request library to download this file path to our computer. We provide request.urlretrieve with two parameters: file url and the filename. For my files, I named them “turnstile_180922.txt”, “turnstile_180901”, etc.
  ```
  download_url = 'http://web.mta.info/developers/'+ link
urllib.request.urlretrieve(download_url,'./'+link[link.find('/turnstile_')+1:])
  ```
  Last but not least, we should include this line of code so that we can pause our code for a second so that we are not spamming the website with requests. This helps us avoid getting flagged as a spammer.
  
  ```
  time.sleep(1)

  ```
  Now that we understand how to download a file, let’s try downloading the entire set of data files with a for loop. The code below contains the entire set of code for web scraping the NY MTA turnstile data.
  
  

