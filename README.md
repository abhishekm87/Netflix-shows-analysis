# Netflix-shows-analysis

Let me get more details about the files in this repository:## Netflix Shows Analysis Repository

This is a **data analysis and visualization project** that examines Netflix's TV shows and movies catalog. Here's what it contains:

### 📊 **Project Overview**
The project analyzes Netflix's OTT (Over-The-Top) content library to uncover patterns and insights about their available titles.

### 📁 **Files**
1. **Neflix_shows_analysis.ipynb** - Main Jupyter Notebook with full analysis
2. **netflix.csv** - Dataset containing 8,807 Netflix titles with 12 columns
3. **README.md** - Project documentation

### 🔍 **Dataset Structure**
The Netflix dataset includes:
- **show_id, type, title** - Basic identifiers
- **director, cast** - Creator information (~30% missing for director)
- **country** - Production country (~9% missing)
- **date_added** - When added to Netflix
- **release_year** - Original release year (ranges from 1925 to 2021)
- **rating** - Content rating (PG, R, TV-14, etc.)
- **duration** - Movie length (minutes) or TV show (seasons)
- **listed_in** - Genres/categories
- **description** - Plot summary

**Dataset size:** 8,807 titles with 4,307 total null values

### 📋 **Analysis Workflow**

The notebook follows a structured data science pipeline:

1. **Data Loading & Exploration**
   - Load CSV data using pandas
   - Examine shape (8,807 x 12) and data types
   - Summary statistics

2. **Data Cleaning**
   - Handle missing values (~30% in director, ~9% in cast/country)
   - Fill categorical nulls with 'Unknown' or 'Other'
   - Drop minimal missing values from date_added
   - Result: Clean dataset with no missing values

3. **Data Transformation**
   - Convert `date_added` to datetime format
   - Split comma-separated genres and countries into lists
   - Extract primary country (first if multiple)
   - Parse duration into numeric value and unit (minutes/seasons)

4. **Exploratory Data Analysis (EDA)**
   - **Movies vs TV Shows**: 6,131 movies vs 2,666 TV shows
   - **Release Year Distribution**: Peak in 2010-2021 (mostly recent content)
   - **Content Ratings**: Distribution by rating category (TV-MA, TV-14, PG, R, etc.)
   - **Top 10 Production Countries**: USA dominates, followed by India, UK, etc.
   - **Average Release Year by Type**: Comparison between movies and TV shows

5. **Visualizations**
   - Count plots (Movies vs TV Shows)
   - Histograms (Release year distribution)
   - Bar charts (Top countries, Ratings)
   - Line charts (Average metrics by type)

### 💡 **Key Insights**
- Netflix has **more movies than TV shows** (69% vs 31%)
- Content is heavily biased toward **recent years** (most from 2013-2021)
- **USA** is the dominant production country
- Significant **data quality issues** with missing director/cast info
- Different duration formats: movies use minutes, TV shows use seasons

### 🛠️ **Technologies Used**
- **Python 3.14.0**
- **pandas** - Data manipulation and analysis
- **numpy** - Numerical operations
- **matplotlib** - Plotting and visualization
- **seaborn** - Statistical visualizations
- **Jupyter Notebook** - Interactive development

This is a solid **beginner to intermediate** data analysis project demonstrating core skills in data cleaning, EDA, and visualization!
