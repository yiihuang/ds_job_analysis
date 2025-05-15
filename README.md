# Data Science Job Market Analysis

## Project Overview

This project analyzes the Data Science job market in India using data scraped from [Naukri.com](https://www.naukri.com/).  
It includes the following pipeline:

1. Web scraping of job postings using Selenium.
2. Data cleaning and preprocessing.
3. Exploratory Data Analysis (EDA) to uncover job market trends.

## Dependencies:
- `Python 3.8+`
- `matplotlib`
- `pandas`
- `selenium`

## Step-by-Step Instructions
Ensure you have Python 3.8+ installed.

### Step 1: Set up the Virtual Environment
You can set up your environment using **one of the following methods**:

####   🔸 Option A: Using `venv` (recommended)

```bash
python -m venv myenv
source myenv/bin/activate    # On Windows: myenv\Scripts\activate
pip install --upgrade pip
pip install -r requirements.txt
```

####   🔹 Option B: Using conda

```bash
conda create -n myenv python=3.8
conda activate myenv
pip install -r requirements.txt
```
See the <a href="EnvSetupGuide.pdf" target="_blank">setup-guide</a> for further explenation.

### Step 2: Run the Scraper.ipynb
Open `Scraper.ipynb` file using either Method A or Method B.

####   🔸 Method A: Using VSCode (recommended)

> I- Install [VSCode](https://code.visualstudio.com/download) and open it.

> II- Use File > Open Folder to open the project folder.

> III- In the Explorer (🗎 icon on the top left), open `Scraper.ipynb`.

> IV- Select the correct virtual environment. See the <a href="EnvSetupGuide.pdf" target="_blank">setup-guide</a> to activate the environment in VSCode.
  
> V- Run the script.

####   🔹 Method B: Using the Jupyter Notebook Web Interface

> I- Launch the notebook using this command:

```bash
# Run from terminal
jupyter notebook scraper.ipynb
```
> II- Open the file `Scraper.ipynb` through the browser.

> III- Select the correct environment kernel. See the <a href="EnvSetupGuide.pdf" target="_blank">setup-guide</a> to activate enviroment in Jupyter.

> IV- Run the script.

This code scrape job listings from Naukri.com. And output `data_scientist_jobs.csv` will be created with raw job listings.

### Step 3: Clean the Data
Open and run the Job_market_analysis.ipynb notebook. This step involves:

  - Removing duplicates

  - Handling null values

  - Formatting job roles and salary info

### Step 4: Perform EDA
Continue in the same notebook to:

  - Visualize common job titles, skills, locations, and companies.

  - Analyze salary trends and required experience levels.

  - Uses matplotlib for plotting insights.


### Step 5: Cluster the locations of the jobs
Continue in the same notebook to:

  - clean job locations into neat strings

  - convert strings to numeric vectors

  - since numeric vectors are high dimensional, reduce their dimensions

  - plot the PCA and UMAP coordinates of the locations and see how they are grouped together
    - each data point is a location. Grouped clusters are similar locations

