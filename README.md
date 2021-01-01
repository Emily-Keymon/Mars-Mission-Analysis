# Mars Mission Analysis
The goal of this project was to develop a webpage to present scraped data from several NASA Mars Mission websites. Python with Splinter, BeautifulSoup, and Pandas, and MongoDB were used to scrape and store the required data, and Python with Flask was used to automate those processes. HTML with Bootstrap CSS was used to generate and format the completed webpage presenting the scraped data.

![mission_to_mars](Images/mission_to_mars.png)

---
## Data Sources
* [NASA Mars News Site](https://mars.nasa.gov/news/) 
* JPL Featured Space Image [here](https://www.jpl.nasa.gov/spaceimages/?search=&category=Mars)
* Mars Facts webpage was visited [here](https://space-facts.com/mars/)
* The USGS Astrogeology site [here](https://astrogeology.usgs.gov/search/results?q=hemisphere+enhanced&k1=target&v1=Mars) 

---
## Tools Used
* Jupyter Notebook
* Python - Pandas, Browser from splinter, BeautifulSoup from bs4, Flask, PyMongo, Datetime
* PyCharm - Python IDE
* MongoDB
* HTML, CSS

---
## Tasks
### Scraping
1.  Created a connection to the Google Chrome browser.
2.  Loaded the Mars news webpage in the browser and scrape the data.
3.  Parsed the HTML data, and extract the title and summary of the latest article.
4.  Loaded the Mars images webpage in the browser and scrape the data.
5.  Parsed the HTML data, and extract the link of the latest Mars featured image.
6.  Loaded the Mars facts webpage in the browser and scrape the data.
7.  Parsed the HTML data, and extract the table of the latest Mars facts.
8.  Loaded the Mars hemisphere webpages in the browser and scrape the data from each page.
9.  Parsed the HTML data from each page, and extract the links of the latest Mars hemisphere images.
10. Compiled all of the extracted data into a Python dictionary.


### Step 2 - MongoDB and Flask Application
1.  The Jupyter notebook was converted into a Python script called `scrape_mars.py` with a function called `scrape` that executed all of the scraping code from above and returned one Python dictionary containing all of the scraped data.
2. A route was created called `/scrape` that imported `scrape_mars.py` script and called the `scrape` function.
3. Return value stored in Mongo as a Python dictionary.
4. A root route `/` was created that queried the Mongo database and passed the mars data into an HTML template to display the data.
5. A template HTML file called `index.html` was creted that took the mars data dictionary and displayed all of the data in the appropriate HTML elements. 
6. Bootstrap was used to structure the HTML template.

---
## Results
 ![Mission_to_Mars_screenshot](https://user-images.githubusercontent.com/64673015/103445542-34599680-4c3b-11eb-9038-2f4680dc2e4e.PNG)
 
 ---
 ## Run
 * http://localhost:5000/ (Python Flask App and MongoDB must be running on the local machine to enable full site functionality.)






