### Web Scrapping:

Web scraping is used for contact scraping, and as a component of applications used for web indexing, web mining and data mining, online price change monitoring and price comparison, product review scraping (to watch the competition), gathering real estate listings, weather data monitoring, website change detection, research, tracking online presence and reputation, web mashup and, web data integration.

### Prevent getting blocked

https://www.scrapehero.com/how-to-prevent-getting-blacklisted-while-scraping/

https://www.youtube.com/watch?v=Bg9r_yLk7VY

### Beautiful Soup

https://www.crummy.com/software/BeautifulSoup/


We start by importing the following libraries:
```
import requests
import urllib.request
import time
from bs4 import BeautifulSoup
```

Next, we set the url to the website and access the site with our requests library:
```
url = 'http://web.mta.info/developers/turnstile.html'
response = requests.get(url)
```

Next we parse the html with BeautifulSoup so that we can work with a nicer, nested BeautifulSoup data structure. If you are interested in learning more about this library, check out the BeatifulSoup documentation.

```
soup = BeautifulSoup(response.text, “html.parser”)
```

We use the method .findAll to locate all of our <a> tags.

```
soup.findAll('a')
```
  
Next, let’s extract the actual link that we want. Let’s test out the first link:
```
one_a_tag = soup.findAll(‘a’)[38]
link = one_a_tag[‘href’]
```
  
```
download_url = 'http://web.mta.info/developers/'+ link
urllib.request.urlretrieve(download_url,'./'+link[link.find('/turnstile_')+1:])
```
  
Last but not least, we should include this line of code so that we can pause our code for a second so that we are not spamming the website with requests. This helps us avoid getting flagged as a spammer.
```
  time.sleep(1)
  ```
  
  ENTIRE CODE:
  ```
  # Import libraries
import requests
import urllib.request
import time
from bs4 import BeautifulSoup

# Set the URL you want to webscrape from
url = 'http://web.mta.info/developers/turnstile.html'

# Connect to the URL
response = requests.get(url)

# Parse HTML and save to BeautifulSoup object¶
soup = BeautifulSoup(response.text, "html.parser")

# To download the whole data set, let's do a for loop through all a tags
line_count = 1 #variable to track what line you are on
for one_a_tag in soup.findAll('a'):  #'a' tags are for links
    if line_count >= 36: #code for text files starts at line 36
        link = one_a_tag['href']
        download_url = 'http://web.mta.info/developers/'+ link
        urllib.request.urlretrieve(download_url,'./'+link[link.find('/turnstile_')+1:]) 
        time.sleep(1) #pause the code for a sec
    #add 1 for next line
    line_count +=1
  ```
