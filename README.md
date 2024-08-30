# BFI Box Office Figures

## The Idea
I have produced a Jupyter notebook which loads data from [BFI's weekly box office figure files](https://www.bfi.org.uk/industry-data-insights/weekend-box-office-figures) and combines them into a dataframe for further analysis. This would allow a user to analyse how individual films have performed in the box office over a period of time.

I have enhanced this data by extracting genre information from [The Movie Database (TMDB)](https://www.themoviedb.org/) API.

## Value
- Prepares data in a format which analysts can easily use.
- Can quickly load data from multiple files, allowing users to view data from across a large time period.
- Adds genre information, which provides potential insights. For example, a user could view how different horror films are performing, or compare the number of films from each genre in the top 15.

## Further Development
- Extract more attributes from the TMDB API.
- Improve the search API request. For example, some films are not found using the search request due to additional information in BFI's "Film" column. A first step would be to exclude anything in brackets from the request query.

## Instructions
GitHub Codespaces can be used to run the Jupyter Notebook:
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/fancyduck5000/box-office-figures?quickstart=1)


<img src="https://www.themoviedb.org/assets/2/v4/logos/v2/blue_square_1-5bdc75aaebeb75dc7ae79426ddd9be3b2be1e342510f8202baf6bffa71d7f5c4.svg" alt="drawing" width="50" height="15"/> This application uses TMDB and the TMDB APIs but is not endorsed, certified, or otherwise approved by TMDB.
