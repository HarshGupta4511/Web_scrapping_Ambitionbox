# Web Scraping AmbitionBox Companies Data

## Project Overview

This project uses Python web scraping techniques to collect company information from AmbitionBox. The scraper sends HTTP requests to AmbitionBox company listing pages, extracts relevant company details using BeautifulSoup, and stores the collected information in a structured Pandas DataFrame for further analysis.

### Skills Demonstrated

* Web Scraping
* HTML Parsing
* Data Collection
* Data Cleaning
* Data Storage using Pandas
* Working with Multiple Web Pages

---

## Features

The scraper collects the following information from AmbitionBox company listings:

* Company Name
* Company Rating
* Reviews Count
* Company Type
* Headquarters Location
* Salary Information
* Interview Information
* Benefits Information
* Jobs Count
* Photos Count

---

## Technologies Used

| Technology          | Purpose                 |
| ------------------- | ----------------------- |
| Python              | Programming Language    |
| Requests            | Sending HTTP Requests   |
| BeautifulSoup (bs4) | HTML Parsing            |
| Pandas              | Data Storage & Analysis |
| LXML                | Fast HTML Parser        |
| Jupyter Notebook    | Development Environment |

---

## Project Structure

```text
Web_scrapping_ambitionbox.com.ipynb
│
├── Import Libraries
├── Send HTTP Requests
├── Parse HTML Content
├── Extract Company Information
├── Store Data in DataFrame
└── Perform Basic Analysis
```

---

## Installation

Install the required libraries before running the notebook:

```bash
pip install pandas requests beautifulsoup4 lxml
```

---

## How It Works

### Step 1: Import Required Libraries

```python
import pandas as pd
import requests
from bs4 import BeautifulSoup
```

### Step 2: Send HTTP Requests

The scraper sends requests to AmbitionBox pages using custom headers to mimic a browser.

```python
requests.get(url, headers=headers)
```

### Step 3: Parse HTML Content

BeautifulSoup converts the webpage source code into a searchable structure.

```python
soup = BeautifulSoup(web_page, "lxml")
```

### Step 4: Extract Company Details

The scraper identifies company cards and extracts required information.

```python
companies = soup.find_all("div", class_="companyCardWrapper")
```

### Step 5: Store Data

The extracted information is stored in a Pandas DataFrame.

```python
final = pd.DataFrame()
```

### Step 6: Combine Multiple Pages

The scraper loops through multiple pages and appends the extracted data into a single dataset.

```python
for page in range(1,101):
    ...
```

---

## Sample Output

| Company Name | Rating | Reviews      |
| ------------ | ------ | ------------ |
| Company A    | 4.2    | 10k+ Reviews |
| Company B    | 3.9    | 5k+ Reviews  |
| Company C    | 4.1    | 8k+ Reviews  |

---

## Dataset Information

The collected dataset contains company-related information from AmbitionBox listings.

The dataset can be used for:

* Exploratory Data Analysis (EDA)
* Data Cleaning Practice
* Data Visualization
* Business Intelligence Projects
* Data Science Learning Projects

---

## Project Limitation

The AmbitionBox company listing contains approximately **500 pages** of company data.

Due to hardware and performance limitations of my device, this project scraped and processed only the **first 100 pages**.

Despite this limitation, the collected dataset still contains a large number of company records and is sufficient for learning:

* Web Scraping
* Data Collection
* Data Processing
* Data Analysis

The code can easily be modified to scrape additional pages on systems with higher computational resources.

---

## Website Preview

### AmbitionBox Homepage

Add your screenshot inside the `images` folder:

```text
Project/
│
├── Web_scrapping_ambitionbox.com.ipynb
├── README.md
└── images/
    └── img1
    └── img2
```

Display it in the README using:

<img width="1918" height="911" alt="Screenshot 2026-06-18 142147" src="https://github.com/user-attachments/assets/e83e1d40-3837-46ed-8aef-0bcd007de3e7" />
<img width="1917" height="790" alt="Screenshot 2026-06-18 141931" src="https://github.com/user-attachments/assets/ce2e24b1-7a5a-4c35-9865-2b4db3bc6246" />

---

## Data Source

**Website Used:**

https://www.ambitionbox.com/list-of-companies

AmbitionBox is a platform that provides company reviews, ratings, salary information, interview experiences, and workplace insights.

---

## Learning Outcomes

Through this project, I learned:

* Sending HTTP requests using Requests
* Understanding webpage structures
* Extracting data using BeautifulSoup
* Working with HTML tags and attributes
* Creating and managing DataFrames with Pandas
* Handling multi-page scraping
* Building datasets for Data Analysis projects
* Understanding real-world data collection workflows

---

## Future Improvements

* Export data directly to CSV files
* Export data to Excel files
* Implement exception handling
* Handle missing values automatically
* Add logging functionality
* Use Selenium for dynamically loaded content
* Store scraped data in SQL databases
* Automate scraping using scheduling tools

---

## Disclaimer

This project was developed solely for educational and learning purposes.

Users should always review and follow a website's Terms of Service and robots.txt guidelines before scraping data from any website.

---

## Author

### Harsh Gupta

**B.Tech Engineering Student**
**Aspiring Data Scientist**

### Skills

* Python
* Pandas
* NumPy
* SQL
* Machine Learning
* Data Analysis
* Web Scraping

---

⭐ If you found this project useful, feel free to star the repository.

