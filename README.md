# IMDB Movie Data Analysis

An exploratory analysis of 1,000 popular IMDB movies released between 2006 and 2016. The notebook works through a set of pandas exercise questions about ratings, votes, revenue, runtime, directors and genres, and plots the answers with seaborn and matplotlib.

## What the notebook covers

- First look at the data: first and last rows, shape, column info and summary statistics
- Data quality: missing values per column (with a heatmap) and a duplicate check
- Films with a runtime of 180 minutes or more, and the 10 longest films
- Average votes and average revenue per year
- Average rating per director, and the 10 highest rated films with their directors
- The 10 highest grossing films
- Number of films per year and average rating per year
- Rating vs revenue scatter plot
- Grouping films into rating bands (7.0 and above, 6.0 and below, and in between) and counting them per year
- How often each genre appears (a film can belong to several genres)

Charts used: pie charts, bar plots, a count plot, a scatter plot and a missing-value heatmap.

## Findings

Taken from the outputs saved in the notebook:

- The dataset has 1,000 rows and 12 columns. Revenue is missing for 12.8% of the films and Metascore for 6.4%. There are no duplicate rows.
- 2016 has by far the most films (297), followed by 2015 (127).
- Average votes per film are highest for 2012 (about 285,000) and lowest for 2016 (about 49,000).
- Average revenue per film is highest for 2009 (about 112.6 million) and lowest for 2016 (about 54.7 million).
- The average rating per year is highest for 2007 (7.13) and lowest for 2016 (6.44).
- Star Wars: Episode VII - The Force Awakens has the highest revenue (936.63 million), followed by Avatar and Jurassic World.
- The Dark Knight is the highest rated film (9.0), and Christopher Nolan directed 5 of the 10 highest rated films.
- Grindhouse is the longest film at 191 minutes. Five films run for 180 minutes or more.
- 445 films are rated 7.0 or higher and 210 are rated 6.0 or lower.
- Drama is the most common genre (513 films), followed by Action (303) and Comedy (279).

## Dataset

`IMDB-Movie-Data.csv` holds 1,000 movies with these columns: Rank, Title, Genre, Description, Director, Actors, Year, Runtime (Minutes), Rating, Votes, Revenue (Millions) and Metascore.

Source: [IMDB data from 2006 to 2016](https://www.kaggle.com/datasets/PromptCloudHQ/imdb-data) on Kaggle.

## Tech stack

- Python
- Jupyter Notebook
- pandas
- seaborn
- matplotlib

## Project structure

```
IMDB-Analysis/
├── imdb-analysis.ipynb   # the analysis, with outputs
├── IMDB-Movie-Data.csv   # dataset
├── requirements.txt
└── LICENSE
```

## Running it

The notebook can be read directly on GitHub with all charts. To run it yourself:

```bash
git clone https://github.com/Hamza-Tahirr/IMDB-Analysis.git
cd IMDB-Analysis
python -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook imdb-analysis.ipynb
```

The notebook reads `IMDB-Movie-Data.csv` from the same folder, so keep the two files together. It was first run on Kaggle with Python 3.7. It also runs on current pandas and seaborn, which print a few deprecation warnings.

## License

The notebook is MIT licensed, see [LICENSE](LICENSE). The dataset comes from Kaggle and is subject to its own terms.
