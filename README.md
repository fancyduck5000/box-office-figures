# BFI Box Office Figures

## The Idea
I have produced a Jupyter notebook which loads data from [BFI's weekly box office figure files](https://www.bfi.org.uk/industry-data-insights/weekend-box-office-figures) and combines them into a dataframe for further analysis. This would allow a user to analyse how individual films have performed in the box office over a period of time.

I have enhanced this data by extracting genre information from [The Movie Database (TMDB)](https://www.themoviedb.org/) API.

It is written in Python and heavily utilises the pandas library. Step-by-step detail can be found as comments within the notebook. The notebook was developed in VSCode, in a GitHub Codespaces environment.

## Value
- Prepares data in a format which analysts can easily use.
- Can quickly load data from multiple files, allowing users to view data from across a large time period.
- Adds genre information, which provides potential insights. For example, a user could view how different horror films are performing, or compare the number of films from each genre in the top 15.

## Further Development
- Extract more attributes from the TMDB API.
- Improve the search API request. For example, some films are not found using the search request due to additional information in BFI's "Film" column. A first step would be to exclude anything in brackets from the request query.
- Furthermore, the first result from the TMDB search may not always contain the correct data, so I would investigate how other attributes from the BFI files could be used to ensure an accurate TMDB search.
- The notebook will currently create a new API call for every film in the dataframe, even if that film has already been searched for and the genres identified. I would improve this by utilising caching to store TMDB results/genres, minimising API calls.

## Instructions
### Codespaces setup
GitHub Codespaces can be used to run the Jupyter Notebook:\
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/fancyduck5000/box-office-figures?quickstart=1) \
The following settings can be used: ![image](https://github.com/user-attachments/assets/fdc83bce-96a9-4777-a354-2c9f736cde48) \
Once you have created the Codespace, it will take a few minutes for the requirements to install.

The notebook can be found in /workspaces/box-office-figures/notebooks/Box_Office_Figures.ipynb

If you try to run a cell of the notebook, you will be asked to select a kernel. Please select "Python Environments..." > "Python (version number)" \
![image](https://github.com/user-attachments/assets/2b5144fa-83e8-4ac5-a449-77f56be277f9)
![image](https://github.com/user-attachments/assets/23835940-7c81-4612-9322-df400902f00d)

### TMDB API Access Token
An access token is required to access the TMDB API. Steps to obtain this:
1. [Create a TMDB account](https://www.themoviedb.org/signup)
2. Go to https://www.themoviedb.org/settings/api
3. In the Create tab, select Developer
4. Read and accept the terms of use.
5. Fill in the form:\
   Type of Use: Personal\
   Application Name: Box Office Figures\
   Application URL: https://github.com/fancyduck5000/box-office-figures \
   Application Summary: Personal analysis of BFI box office figures\
   Fill in your personal details and Submit
7. Copy your Read Access Token
8. In GitHub, click on your avatar in the top right hand corner
9. Click on Settings
10. Under Code, planning, and automation, click on Codespaces
11. Create a new secret with the name "TMDB_READ_ACCESS_TOKEN". Paste your Read Access Token as the value.
12. Under repository access, put "fancyduck5000/box-office-figures"

**Alternatively, if you do not want to create an access token, you can view the output of a full notebook run in notebooks/Box_Office_Figures.html. This is best downloaded and viewed in a browser.**






## Attributions
- <img src="https://www.themoviedb.org/assets/2/v4/logos/v2/blue_square_1-5bdc75aaebeb75dc7ae79426ddd9be3b2be1e342510f8202baf6bffa71d7f5c4.svg" alt="drawing" width="50" height="15"/> This application uses TMDB and the TMDB APIs but is not endorsed, certified, or otherwise approved by TMDB.
- This repository is generated from the [codespaces-jupyter](https://github.com/github/codespaces-jupyter) public template.
