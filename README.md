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
### NASA Mars News
1.  Imported Pandas, Browser from splinter and BeautifulSoup from bs4.
2.  Set the executable path and initialize the chrome browser in splinter.
3.  Visited the mars nasa news site.
4.  Converted the browser html to a soup object and then quit the browser.
5.  Parsed content title.
6.  Used the parent element to find the first a tag and save it as `news_title`.
7.  Used the parent element to find the paragraph text.
** JPL 1 - 6**
8.  Read html into a dataframe.
9.  Add columns to the dataframe, index description.
10. Saved dataframe to html.
### JPL
1.  Visited the JPL site.
2.  Found and clicked the full image button.
3.  Found and clicked the more info button.
4.  Parsed the resulting html with soup.
5.  Found the relative image url.
6.  Used the base url to create an absolute url.

## Mars Hemispheres
1.  Visited the Mars Hemispheres site.
2.  Obtained high resolution images for each hemisphere.
3.  Created a list of all of the hemispheres.
4.  Looped through those links, click the link, find the sample anchor, return the href.
5.  Found the elements on each loop to avoid a stale element exception.
6.  Found the Sample image anchor tag and extract the href.
7.  Got Hemisphere title.
8.  Appended hemisphere object to list.
9.  Navigated backwards.
10. Viewed image urls.
11.  Quit browser.




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






