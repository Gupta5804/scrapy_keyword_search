# scrapy_keyword_search 

![alt text](http://www.rawble.com/skin/frontend/sm_market/default/images/logo.png "Rawble")


#### Search for the set of keywords by crawling certain sites and return the results in json format


Prerequisites
--------------
* Install Anaconda (for python). [Download Here](https://www.anaconda.com/download/)
* Install VS code (recommended). [Download Here](https://code.visualstudio.com/)

Installation
--------------

1. Download the repository as a zip file or as a local repository.
2. Extract the Zip file .
3. Open the folder with VS code.
4. Install requirements using `pip install -r requirements.txt` in vs code terminal
(Open vscode terminal using [Ctrl + ` ])

Usage
-------------
In keyword_search > spiders > keyword_spider.py

* Add domains of sites you want to search the keywords in `allowed_domains = []`.

  (If the domain name is "https://www.google.com/" just add google.com)
  
  (Note : Do not add https or www in allowed_domains)
* Example: `allowed_domains = ['google.com','yahoo.com','youtube.com']`


* Similarly Add starting urls of the domains in `start_urls=[]`

  (Add full links of the starting urls from where you want to start crawling)

* Example : `allowed_domains = ["yasham.in","osheaherbals.com"]

    start_urls = ["http://www.yasham.in/","https://www.osheaherbals.com/"]`
    
* Add keywords to search for in `list_keywords=[]`
    
* Now in the command line `scrapy crawl keyword_spider -o output.json`

  (The results will be in Json format)
  
  (Convert it to .xls file using [this](http://www.json-xls.com/json2xls))
