# Buffy the Vampire Slayer: SQL Data Analytics Project

Personal project, completed by Tutuwa Ahwoi in October 2024.

## Project Overview

This project uses SQL to analyze data from the cult classic television show "Buffy the Vampire Slayer". It aims to uncover interesting patterns and insights about the show, its episodes, writers, and ratings through data analysis. It leverages 20+ complex SQL queries, including subqueries and window functions, to analyze trends in ratings, viewership, and engagement.

## Technologies Used

1. Microsoft Excel
    - Used for data cleaning and transformation
    - Used for creating preliminary charts and graphs
2. SQL (PostgreSQL)
    - Chosen as the relational database management system for storing and querying the dataset
    - Used for initial data exploration, basic statistical analysis, and complex queries
    - Leveraged for performing advanced analytical functions and window operations

## Data Sources

The data for this project was collected from the following sources:

1. IMDb (Internet Movie Database)
    - Episode (user) ratings and vote counts
    - Ratings are on a scale of 0 to 10, which is standard for IMDB ratings. 10 is the best, and 0 is the worst.
2. Buffy the Vampire Slayer Wikipedia Page
    - Episode titles
    - Writer and director information
    - Season and episode numbers
    - U.S. viewer numbers for each episode

## **Database Structure**

The project employs a relational database in PostgreSQL to organize the data effectively. The database comprises four interconnected tables:

- **episodes:** Containing core details about each episode, such as the air date, title, and director.
- **writers:** Listing all writers associated with the show.
- **writers_episodes:** Acting as a bridge to link episodes with their respective writers.
- **ratings:** Holding rating information from IMDb (ratings and vote counts) and Wikipedia (U.S. viewer numbers).

## Methodology

1. Data Collection: Gathered U.S. viewer ratings from Wikipedia and IMDB scores for all episodes.
2. Data Cleaning: Used Excel to clean and preprocess the data.
3. Exploratory Data Analysis: Utilized SQL for initial data exploration and basic statistical analysis.
4. Visualization: Created charts and graphs using Excel.

## **Exploratory Data Analysis**

### Identify the average IMDb rating for all episodes

The analysis starts by calculating and displaying the average IMDb rating across all episodes in the dataset. This simple yet informative analysis provides a quick overview of the general quality of episodes as perceived by IMDb users. The result offers a baseline metric that can be used for comparison with individual episode ratings or ratings of specific seasons or shows.

### **Top 10 Most Popular Episodes**

This SQL query identifies and lists the ten episodes with the highest IMDb ratings in the dataset. It provides a quick overview of the most well-received episodes according to IMDb users. This helps to identify peak moments of quality or popularity across the episodes in the show.

### **Top 10 Least Popular Episodes**

This SQL query identifies and displays the ten episodes with the lowest IMDb ratings in the dataset. It offers a glimpse into the least popular or critically acclaimed episodes according to IMDb users. This provides insight into some of the show’s potential weak points.

### Analyze the distribution of ratings

This SQL query analyzes the distribution of IMDb ratings for episodes in the "Buffy the Vampire Slayer" dataset. It groups episodes by their rounded IMDb rating (to the nearest integer) and counts how many episodes fall into each rating bracket. The results offer a clear picture of the overall quality perception of the show's episodes, highlighting which rating ranges are most common.

## Additional Key Queries

- Episode analysis by season and overall series trends
- Director impact on episode ratings
- Writer contribution and patterns
- Correlation between viewership numbers and IMDb ratings
- Relationship between “Big Bad” (main villains) and IMDb ratings

## Key Insights

My analysis revealed several interesting patterns and insights:

**Overall Ratings and Viewership:**

- **Episode Quality**: The IMDb ratings range from a minimum of 6.3 to a maximum of 9.7 (out of 10), with an average IMDb rating of 8.01 for all episodes. A majority of episodes fall within the 7-8 range, indicating most episodes were well-received by the audience.
- **Viewership:** Viewership peaked in the early seasons (2-3) and showed a general declining trend afterwards.
    - Highest Average viewership: Season 3 (6.10m)
    - Lowest Average viewership: Season 1 (3.63m).

**Season Analysis:**

- **Seasonal Patterns**: The show maintained consistently high ratings throughout its run, with all seasons averaging above 7.5. Season 3 had the highest average rating of 8.32/10, closely followed by Season 5 at 8.06/10.
- **Season Premieres and Finales**: The analysis reveals a pattern of season finales outperforming premieres in terms of ratings, suggesting the show excelled at delivering satisfying conclusions. The premiere ratings fluctuate between 7.6 and 8.1, while finale ratings have a wider range from 8.6 to 9.5. The series finale (the very final episode of the show) also had the third highest finale rating of 9.3, indicating that fans were generally satisfied with the conclusion of the show.
- **The Power of the "Big Bad":** Examining the correlation between the season's main villain ("Big Bad") and ratings revealed that Season 3, featuring Mayor Richard Wilkins, stood out with the highest average rating and a significantly higher z-score compared to other seasons. This suggests that the "Big Bad" significantly impacts a season's reception.

**Writer and Director Contributions**

- **Joss Whedon's Influence**: As the creator and a prolific writer for the show,  Joss Whedon's episodes consistently garner high ratings, highlighting his significant impact on the show's quality.  Joss Whedon-written episodes had an average rating of 8.58/10, significantly higher than the series average of 8.01/10, and of the other writers for the show.
- **Writer Impact**: The analysis also acknowledges the contributions of other talented writers, such as Marti Noxon, Jane Espenson, Drew Goddard, and Douglas Petrie, showcasing the show's success as a collaborative effort.
- **Director Influence**: Episodes directed by Joss Whedon had the highest average rating (8.84/10) among directors with more than five episodes. Michael Gershman, who directed 10 episodes, had the second highest average rating of 8.26/10. Nick Marck also contributed significantly to the show's high production value.

**Viewership and IMDb Ratings**

- While a general trend indicates that higher-rated episodes attract more viewers, the correlation isn't consistently strong across all seasons. In general, there is no strong correlation between user ratings and viewership numbers. This suggests that other factors beyond episode quality, such as scheduling and promotion, or even cultural trends, can influence viewership.

## Conclusion
Buffy the Vampire Slayer maintained a consistent level of quality throughout its run, thanks to strong writing, directing, and the contributions of a talented team of creators. The show's true legacy lies in its ability to resonate with viewers on an emotional level, inspiring a devoted fan base that continues to celebrate it today. 

The show maintained consistently high IMDb ratings throughout its run, with an average rating of 8.01/10. While viewership declined in later seasons, the show's quality remained strong, indicating a loyal core audience.

## Acknowledgments

- Data sourced from IMDb and Wikipedia
- Inspired by the work of Joss Whedon and the Buffy the Vampire Slayer creative team


**Data Sources**

- Ratings: https://www.imdb.com/title/tt0118276/ratings/
- Episodes: https://en.wikipedia.org/wiki/List_of_Buffy_the_Vampire_Slayer_episodes#Ratings
- IMDB Vote Count: https://www.imdb.com/title/tt0118276/episodes/?season=1

## Additional Information
Further information about this project can be found [on this blog post](https://www.tutuwaahwoi.com/blog/data-analysis-a-sql-analysis-of-episode-ratings-of-buffy-the-vampire-slayer/).
