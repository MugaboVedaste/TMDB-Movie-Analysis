# TMDb Movie Data Analysis Using Python and Pandas

A data analysis project that uses the TMDb API, Python, and Pandas to explore movie financial performance, ratings, popularity, franchises, and directors.

## Project Overview

This project demonstrates a data analysis workflow involving API data extraction, data cleaning, KPI analysis, and visualization.

### Objectives

- Collect movie information from the TMDb API.
- Clean and transform movie data using Pandas.
- Rank movies by revenue, budget, profit, ROI, ratings, votes, and popularity.
- Perform searches based on actors, directors, and genres.
- Compare franchise performance and analyze directors.
- Visualize relationships and trends using Matplotlib.

## Technologies Used

- Python
- Pandas
- NumPy
- Requests
- Matplotlib
- Jupyter Notebook
- python-dotenv
- Git and GitHub
- TMDb API

## Project Structure

```text
TMDB-Movie-Analysis/
├── notebooks/
│   ├── 01_data_extraction.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_implementation_and_analysis.ipynb
│   └── 04_data_visualization.ipynb
├── data/
│   ├── raw/
│   └── processed/
├── reports/
│   ├── figures/
├── .env
├── .env.example
├── .gitignore
├── requirements.txt
└── README.md
```

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/MugaboVedaste/TMDB-Movie-Analysis.git
cd TMDB-Movie-Analysis
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it in Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

If you use Git Bash:

```bash
source .venv/Scripts/activate
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Configure the TMDb API token

Create a `.env` file in the project root:

```text
TMDB_READ_ACCESS_TOKEN=your_tmdb_read_access_token
```

Replace the placeholder with your own TMDb API read access token.

**Security:** Never commit `.env` or publish your API token. The `.env` file should be listed in `.gitignore`.

### 5. Run the notebooks

Start Jupyter:

```bash
jupyter notebook
```

Alternatively, open the project in Visual Studio Code and select your `.venv` Python interpreter.

Run the notebooks in this order:

1. `01_data_extraction.ipynb` — retrieves movie details and credits.
2. `02_data_cleaning.ipynb` — cleans the raw dataset and saves the processed data.
3. `03_implementation_and_analysis.ipynb` — calculates KPIs and analyzes movies, franchises, and directors.
4. `04_data_visualization.ipynb` — creates charts and saves figures.

Run the earlier notebooks first if the raw or processed data files are not available.

## Key Analyses

### Movie performance

- Highest and lowest revenue.
- Highest production budgets.
- Highest and lowest calculated profit.
- Highest and lowest revenue-to-budget ratios for eligible movies.
- Most voted, highest rated, lowest rated, and most popular movies.

### Advanced searches

- Science Fiction and Action movies starring Bruce Willis.
- Movies starring Uma Thurman and directed by Quentin Tarantino.

### Franchise and director analysis

- Franchise movie counts, budgets, revenues, and mean ratings.
- Director movie counts, total recorded revenue, and mean ratings.
- Comparison between movies with recorded collections and those without them.

### Visualizations

- Revenue versus budget.
- Median revenue-to-budget ratio by genre.
- Popularity versus rating.
- Combined revenue by release year.
- Franchise versus non-franchise mean revenue.

## Important Metric Definitions

**Profit**

`Profit = Revenue - Budget`

**Revenue-to-budget ratio**

`Ratio = Revenue / Budget`

A ratio of `3.0` means the movie generated three times its production budget in revenue. This ratio is not equivalent to net profit or a complete ROI calculation.

Budgets and revenues are expressed in millions of US dollars in the processed dataset.

## Data and Limitations

The analysis covers a selected set of movies, not the entire movie industry. Missing values and the limited sample size may affect comparisons. Collection membership is based on the collection information recorded by TMDb.


## Author

**Vedaste MUGABO**

GitHub: [MugaboVedaste](https://github.com/MugaboVedaste/TMDB-Movie-Analysis)

## Acknowledgment

Movie information is provided by [The Movie Database (TMDb)](https://www.themoviedb.org/).

This project uses TMDb data but is not endorsed or certified by TMDb.
