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

## Setup OpenAI API Key

This project uses OpenAI's API for data cleaning and analysis. Follow these steps to set up your API key:

1. Create a `.env` file in the project root directory
2. Add your OpenAI API key to the file in this format:
   ```
   OPENAI_API_KEY=your_api_key_here
   ```

### Getting Your API Key

1. Go to https://platform.openai.com and create an account
2. Make sure you are logged in
3. Click on `dashboard` at the top-right
4. At the very left click on `API keys`
5. Click on `create new secret key`
6. Click on `Copy`
7. Paste into `.env` file after `OPENAI_API_KEY=` (No space before or after)

### ⚠️ Important Security Notes

1. **Protect Your API Key**: 
   - The `.env` file is already added to `.gitignore`
   - NEVER commit your API key to GitHub
   - NEVER share your API key with others
   - If you accidentally expose your key, regenerate it immediately

2. **Set Usage Limits**:
   To avoid unexpected charges, set a usage threshold:
   1. Click on the gear icon at the top right of OpenAI platform
   2. Click on `Billing` at the very left side
   3. Click on `Usage limits`
   4. Set a dollar amount in `Set Higher Threshold Alert`
   - Recommended: Start with $1 and increase if needed
   - You will never be charged more than this limit

