# veefyed-data-analyst-technical-assessment

## Task instructions
https://veefyed-my.sharepoint.com/:b:/r/personal/esme_antwi_veefyed_com/Documents/Veefyed%20Senior%20Data%20Analyst%20Task.pdf?csf=1&web=1&e=2TJJTM


## Day 1 Deliverables
1. Csv file - products.csv
2. Script file - scrape_products.ipynb
3. Tools Used
    Python: Contains helpful tools for web scraping.
    requests module: Utilized this to request content from the website.
    BeautifulSoup: Provided useful methods to parse and utilize html content from the website.
    regex: Used to match patterns that weren't easily available to retrieve.
    csv module: Used to persist dictionary to csv file.

4. #### Issues Encountered
    - Ingredients list aren't structured appropriately. I used a little involved logic to retrieve them.

5. #### Assumptions and Logic Applied
    - I made a choice to scrape cleansing products.
    - Picked the url manually and used Python's request module to retrieve the page content.
    - I used BeautifulSoup to parse the content and retrieve individual elements listed.
    - Some of the required details were pretty straightforward (name, brand, url, image).
    - Others were a little complex to retrieve. I utilized a second layer to retrieve each product's details with a request to their urls.
        - Used two methods, name splitting, and single product call to retrieve size
        - Used a custom logic to gather product categories.

6. #### How the Dataset was Organized
    Step 1: I created a dictionary to store the initial product retrieval from the cleansing products page.
    Step 2: I made individual requests to each product url and updated the dictionary to include missing details from step 1.
    Step 3: Utilized the csv module to persist the dictionary data into a csv file.