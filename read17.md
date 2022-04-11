# Web scraping 

## What is Web scraping 
Web scraping a web page involves fetching it and extracting from it. While web scraping can be done manually by a software user, the term typically refers to automated processes implemented using a bot or web crawler. The content of a page may be parsed, searched, reformatted, its data copied into a spreadsheet or loaded into a database.

Web pages are built using text-based mark-up languages (HTML and XHTML) and frequently contain a wealth of useful data in text form. Most web pages are designed for human end-users and not for ease of automated use, so specialized tools and software have been developed to facilitate the scraping of web pages. Web scraping is used for contact scraping, and as a component of applications used for web indexing, web mining and data mining.

## Techniques

Even the best web-scraping technology cannot replace a human's manual examination and copy-and-paste. Sometimes this may be the only workable solution when websites explicitly set up barriers to prevent machine automation. Text pattern matching is a simple yet powerful approach to extract information from web pages. Static and dynamic web pages can be retrieved by posting HTTP requests to the remote web server using socket programming.

Many websites have large collections of pages generated dynamically from an underlying structured source like a database. In data mining, a program that detects such templates in a particular information source, extracts its content and translates it into a relational form is called a wrapper. Some semi-structured data query languages, such as XQuery and the HTQL, can be used to parse HTML pages and to retrieve and transform page content.

**Important notes about web scraping:**
Read through the website’s Terms and Conditions to understand how you can legally use the data. Most sites prohibit you from using the data for commercial purposes.
Make sure you are not downloading data at too rapid a rate because this may break the website. You may potentially be blocked from the site as well.

## How to Scrape Websites Without Getting Blocked

Web Crawlers can retrieve data much quicker, in greater depth than humans, so bad scraping practices can have some impact on the performance of the site. Some sites use measures that can lead to web scraping getting blocked, because they do not believe in open data access. If a crawler performs multiple requests per second and downloads large files, an under-powered server would have a hard time keeping up with requests from multiple crawlers.

- Basic Rule: “Be Nice”

- Respect Robots.txt
Web spiders should ideally follow the robot.txt file for a website while scraping. It has specific rules for good behavior, such as how frequently you can scrape. Some websites allow Google to scrape their websites, by not allowing other sites to scrape them. This goes against the open nature of the Internet and may seem unfair.

- Make the crawling slower, do not slam the server, treat websites nicely

The faster you crawl, the worse it is for everyone. If a website gets too many requests than it can handle it might become unresponsive. Use auto throttling mechanisms which will automatically throttle the crawling speed based on the load on both the spider and the website that you are crawling.

- Do not follow the same crawling pattern

Websites with intelligent anti-crawling mechanisms can easily detect spiders by finding patterns in their actions. Web scraping bots tend to have the same crawling specified. Incorporate some random clicks on the page, mouse movements and random actions that will make a spider look like a human.

- Make requests through Proxies and rotate them as needed

Multiple requests coming from the same IP will lead you to get blocked, so we need to use multiple addresses. When we send requests from a proxy machine, the target website will not know where the original IP is from.


**Rotate User Agents and corresponding HTTP Request Headers between requests**

Every request made from a web browser contains a user-agent header and using the same User-agent consistently leads to the detection of a bot. Most web scrapers do not have a User Agent by default, and you need to add that yourself. If you find your bots getting blocked even after putting in a recent User-Agent string, you should add some more request headers.

**Use a headless browser like Puppeteer, Selenium or Playwright**

## How does web scraping function 

- Step 1: Making an HTTP request to a server

- Step 2: Extracting and parsing the website’s code

- Step 3: Saving the relevant data locally

## How to scrape the web (step-by-step)
- Step one: Find the URLs you want to scrape

- Step two: Inspect the page 

- Step three: Identify the data you want to extract


- Step four: Write the necessary code  

- Step five: Execute the code

- Step six: Storing the data

## What tools can you use to scrape the web?

- BeautifulSoup 

- Scrapy

- Pandas 

- Parsehub

