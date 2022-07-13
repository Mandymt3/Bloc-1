# Project Plan your trip with Kayak
The objective is to recommend the best destinations and hotels for users of Kayak based on weather and hotels in the area. This project focused mainly on the first phase: the data collection, including scraping data from destinations, getting weather data from each destination, getting hotels' info about each destination, storing all the information above in a data lake, and extraction, transformation, and loading cleaned data from the data lake to a data warehouse.

# Prerequisites
## Selenium environment setup

1. Why use selenium?
* In the beginning, when I used libraries Request and Beautifulsoup directly for web scraping, I couldn't locate the tag, so I used selenium, to avoid the impact of javascript in the HTML of bookings page.

2. Install Selenium
* First, download and install libraries selenium in jupyter notebook.
```python
!pip install selenium
```
3. Install the browser driver
* The following is based on the chrome browser to install the browser driver.
*	The first step is to know the version of the browser. Chrome version information can be found in "Settings->About Chrome".
![image](https://user-images.githubusercontent.com/102224383/178761874-61eec7eb-fdbc-4df6-a1ae-4bddbe0be483.png)
*	After finding the browser version, go to https://chromedriver.chromium.org/downloads to download the corresponding chrome driver.
![image](https://user-images.githubusercontent.com/102224383/178761673-dd49f777-2751-4085-9e28-8f183029e824.png)

4. Windows local environment configuration.

*	Unzip the downloaded chromedriver.exe package and put it in the Application directory under the Google Chrome installation directory 
![image](https://user-images.githubusercontent.com/102224383/178762300-1386bea3-3947-4c94-b26a-630eea13789c.png)
*	Then configure the system environment variable to add the path of chromedriver.exe in Path.
![image](https://user-images.githubusercontent.com/102224383/178762527-be62534d-169e-42fc-affb-a8bb65e3d7bb.png)

# Dataset 
All the csv files in this folder are obtained by web scraping

# Usage
## Kayak_Project.ipynb
This notebook can be used to obtain:
*	A .csv file containing enriched information about weather and hotels for each French city then stored in an S3 bucket
*	Two maps represent a Top-5 destinations and a Top-20 hotels in the area
