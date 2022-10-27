
<a name="readme-top"></a>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/joshmartin33/web-scraping-challenge.git">
    <img src="images/Logo1.webp" alt="Logo1" width="70" height="70">
  </a>

<h3 align="center">web-scraping-challenge</h3>

  <p align="center">
    Mars Data Analysis
    <br />
    <a href="https://github.com/joshmartin33/web-scraping-challenge.git"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/joshmartin33/web-scraping-challenge/blob/main/mars_data_challenge_part_1.ipynb">View Part 1 Analysis</a>
    ·
    <a href="https://github.com/joshmartin33/web-scraping-challenge/blob/main/mars_data_challenge_part_2.ipynb">View Part 2 Analysis</a>
    ·
    <a href="https://github.com/joshmartin33/web-scraping-challenge/issues">Report Bug</a>
  </p>
</div>


<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#prerequisites">Prerequisites</a></li>
        <ul style="list-style-type:square;">
        <li><a href="#installation">Installation</a></li>
      </ul>
    <li><a href="#part-1">Part 1: Scrape</a></li>
      <ul style="list-style-type:square;">
        <li><a href="#getting-started-part-1">Getting Started</a></li>
      </ul>
    <li><a href="#part-2">Part 2: Analyse Mars Weather Data</a></li>
      <ul style="list-style-type:square;">
        <li><a href="#getting-started-part-2">Getting Started</a></li>
      </ul>
    <li><a href="#creators">Creators</a></li>
    <li><a href="#citing-and-referencing">Citing and Referencing</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

<p>I am now ready to take on the full web-scraping and data analysis project for the mission to Mars. I have learned to identify HTML elements on a page, identify their <code>id</code> and <code>class</code> attributes, and use this knowledge to extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup. I have also learned to scrape various types of information. These include HTML tables and recurring elements, like multiple news articles on a webpage.</p>

<ul>
        <li>
            <p>Part 1: Scrape titles and preview text from Mars news articles. Optionally export the data into a JSON file or a MongoDB database.</p>
        </li>
        <li>
            <p>Part 2: Scrape and analyse Mars weather data, which exists in a table.</p>
        </li>
</ul>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---
<!-- Prerequisites -->
### Prerequisites

Required software to be able to run the following steps.
* Jupyter Notebook 
  ```sh
  pip install notebook
  ```
For detailed instructions on how to compleet the install please follow the instructions in the <a href=https://jupyter.org/install>link.</a>


<p align="right">(<a href="#readme-top">back to top</a>)</p>

---
### Installation

1. Install Pandas packages
   ```sh
   pip install pandas
   ```
2. Install Splinter packages
   ```sh
   pip install splinter
   pip install splinter[selenium3]
   ```
3. Install Webdriver Manager packages
   ```sh
   pip install webdriver_manager
   ```
4. Install Beautiful Soup packages
   ```sh
   pip install bs4
   ```
5. Clone the repo
   ```sh
   git clone https://github.com/joshmartin33/web-scraping-challenge.git
   ```
<p align="right">(<a href="#readme-top">back to top</a>)</p>

---
<!-- Part 1 -->
## Part 1

Scrape titles and preview text from Mars news articles. Optionally export the data into a JSON file or a MongoDB database.

<ol>
        <li>
            <p>Create a new Jupyter notebook named <code>mars_data_challenge_part_1.ipynb</code>.</p>
        </li>
        <li>
            <p>Scrape the website by using Splinter and Beautiful Soup. Specifically, scrape the title and preview text, or summary text, of each article on the landing page.</p>
        </li>
        <li>
            <p>Store the scraping results in Python data structures.</p>
            <ul>
                <li>
                    <p>Store all the dictionaries in a Python list.</p>
                </li>
                <li>
                    <p>Print the list in your notebook.</p>
                </li>
            </ul>
        </li>
        <li>
            <p>Optionally, store the scraped data in a file or database (to ease sharing the data with others). To do so, export the scraped data to either a JSON file or a MongoDB database.</p>
        </li>
    </ol>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---
<!-- GETTING STARTED -->
### Getting Started Part 1
<br>
To get a local copy up and running follow these example steps.
<br></br>

<ul>
<li>Open file called mars_data_challenge_part_1 in Jupyter Notebook</li>
<li>Refresh and clear the kernal.</li>
<li>Click on "Run all"</li>
<li>Results will be printed to the screen and results saved as a json file</li>
</ul>


<p align="right">(<a href="#readme-top">back to top</a>)</p>

---
<!-- Part 2 -->
## Part 2

Scrape and analyse Mars weather data, which exists in a table.

<ol>
        <li>
            <p>Create a Jupyter notebook named <code>mars_data_challenge_part_2.ipynb</code>. Import the relevant dependencies for web scraping, Pandas, and Matplotlib.</p>
        </li>
        <li>
            <p>With your automated browser, visit the Mars Temperature Datasite. Note that the URL is <code>https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html</code>.</p>
        </li>
        <li>
            <p>Scrape the data in the HTML table. To do so, choose one of two ways. The first, simpler way is to use Pandas's <code>read_html</code> method. The second, slightly more challenging way is to manually scrape the data by using Splinter and Beautiful Soup. We highly encourage you to choose the latter to reinforce your scraping skills.</p>
        </li>
        <li>
            <p>Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:</p>
            <ul>
                <li>The <code>id</code> heading: The identification number of a single transmission from the Curiosity rover.</li>
                <li>The <code>terrestrial_date</code> heading: The date on Earth.</li>
                <li>The <code>sol</code> heading: The number of elapsed sols (Martian days) since Curiosity landed on Mars.</li>
                <li>The <code>ls</code> heading: The solar longitude.</li>
                <li>The <code>month</code> heading: The Martian month.</li>
                <li>The <code>min_temp</code> heading: The minimum temperature, in Celsius, of a single Martian day (sol).</li>
                <li>The <code>pressure</code> heading: The atmospheric pressure at Curiosity's location.</li>
            </ul>
        </li>
        <li>
            <p>Examine the data types of all the DataFrame columns. If necessary, cast (or convert) the data to the appropriate <code>datetime</code>, <code>int</code>, or <code>float</code> data types.</p>
        </li>
        <li>
            <p>Answer the following question: How many months exist on Mars?</p>
        </li>
        <li>
            <p>Answer the following question: How many Martian (and not Earth) days' worth of data exist in the scraped dataset?</p>
        </li>
        <li>
            <p>Answer the following question: What are the coldest and the warmest months on Mars (at the location of Curiosity)? Get the answer by averaging the minimum daily temperature of all the months. Plot the results as a bar chart.</p>
        </li>
        <li>
            <p>Answer the following question: Which months have the lowest and the highest atmospheric pressure on Mars? Get the answer by averaging the daily atmospheric pressure of all the months. Plot the results as a bar chart.</p>
        </li>
        <li>
            <p>Answer the following question: About how many terrestrial (Earth) days exist in a Martian year? That is, in the time that Mars circles the Sun once, how many days elapse on Earth? Visually estimate the result by plotting the daily minimum temperature.</p>
        </li>
        <li>
            <p>Export the DataFrame to a CSV file.</p>
        </li>
    </ol>


<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

<!-- GETTING STARTED -->
### Getting Started Part 2

To get a local copy up and running follow these example steps.
<br></br>

<ul>
<li>Open file called mars_data_challenge_part_2 in Jupyter Notebook</li>
<li>Refresh and clear the kernal.</li>
<li>Click on "Run all"</li>
<li>Results will be printed to the screen and results saved as a csv file</li>
</ul>


<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

<!-- Creators -->
## Creators

Josh Martin - <a href="https://github.com/joshmartin33">GitHub</a>


<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

<!-- Citing and Referencing -->
## Citing and Referencing

* Mars Planet Scince - Web Scraping. (2022). Retrieved on 23/10/2022 from <a href="https://redplanetscience.com/">Link</a>
* Mission to Mars - Web Scraping. (2022). Retrieved on 23/10/2022 from <a href="https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html">Link</a>


<p align="right">(<a href="#readme-top">back to top</a>)</p>

---