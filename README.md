Your README file is well-structured and clear. Here are some minor corrections and suggestions for improvement:

---

# CinFind: Your Personalized Movie Recommender

---

## Table of Contents
1. [Introduction](#introduction)
2. [Research Questions](#research-questions)
3. [Dataset](#dataset)
4. [Methodology](#methodology)
5. [Results and Findings](#results-and-findings)
6. [Conclusions](#conclusions)
7. [Limitations](#limitations)
8. [Running the Application](#running-the-application)
9. [References](#references)

---

## Introduction
CinFind aims to develop a movie recommendation tool that offers personalized suggestions to enhance user satisfaction. By leveraging cloud, big data, and machine learning technologies, we strive to provide optimal movie recommendations.

---

## Research Questions
1. What factors are more important in movie ratings: critical reviews (Tomatometer scores) or audience preferences?
2. Can we create personalized movie recommendations based on individual user preferences?
3. How accurate can predictive modeling be in predicting movie ratings?
4. What are the potential business outcomes of this project for streaming platforms and movie-aggregation websites?

---

## Dataset
### Source
We sourced our dataset from Rotten Tomatoes, a renowned cinema review-aggregation website. Data was fetched using web scraping techniques with BeautifulSoup and the `rottentomatoes-python` library.

### Storage and Processing
- **Storage:** Using SQLite for efficient data retrieval.
- **Processing:** Essential columns like Title, Tomatometer score, Audience score, Actors, Genre, and Rating were processed to generate results from the ML model.

---

## Methodology
1. **Web Scraping:** Using BeautifulSoup to collect data.
2. **Database Storage:** SQLite database for storing the scraped data.
3. **Data Preprocessing:** Conducting EDA, cleaning data, and converting it into suitable formats using PySpark dataframes.
4. **Predictive Modeling:** Utilizing K-Means clustering to create predictive models.
5. **Deployment:** Deploying the application using Streamlit and Localtunnel.

### Files Needed to Run the Web App
- `movies.db`
- `app.py`

---

## Results and Findings
1. **Reviews Matter:** Both critical reviews (Tomatometer scores) and audience preferences significantly influence movie ratings. Certain genres such as drama and sci-fi tend to have high-rated movies in our dataset.
2. **Predictions:** The K-Means clustering model demonstrates promising cluster creation in estimating similar movies based on features like genre, rating, cast, and title. Streaming platforms and movie-aggregation websites can leverage personalized recommendations to enhance user engagement and satisfaction.

---

## Conclusions
1. Utilized web scraping, relational databases, machine learning, data preprocessing, and web application deployment for creating a personalized movie recommender.
2. Highlighted critical factors influencing movie ratings, genre trends, and the effectiveness of personalized recommendations.
3. Identified future opportunities for further research and integration with PySpark Streaming for real-time data updates.

---

## Limitations
1. **Dependency on Rotten Tomatoes:** This project relies heavily on data from Rotten Tomatoes and the `rottentomatoes-python` library. Any changes to the website's structure or restrictions on data access could impact the functionality of our recommendation system.
2. **Single Data Source:** The current implementation uses only Rotten Tomatoes for movie data. Expanding the data sources to include other movie review sites like IMDb and Metacritic could enhance the recommendation system's accuracy and reliability.

---

## Running the Application
To run the CinFind web application using Streamlit, follow these steps:

1. **Install Necessary Packages:**
   ```bash
   pip install pyspark
   pip install streamlit
   pip install bs4
   pip install rottentomatoes-python
   ```

2. **Navigate to the Project Directory:**
   Ensure you are in the directory containing `movies.db` and `app.py`.

3. **Run the Streamlit Application:**
   ```bash
   streamlit run app.py
   ```

4. **Access the Application:**
   Once the application is running, Streamlit will provide a local URL (e.g., `http://localhost:8501`) where you can interact with the CinFind recommendation system.

---

## References
1. [Rottentomatoes-python Library · PyPI](https://pypi.org/project/rottentomatoes-python/)
2. [Localtunnel for Web Application Hosting](https://github.com/localtunnel/localtunnel)
3. [Machine Learning based Movie Recommendation System](https://hcis-journal.springeropen.com/articles/10.1186/s13673-018-0161-6)
4. [An Efficient movie recommendation algorithm based on improved k-clique methods](https://www.academia.edu/51025889/A_Research_Paper_on_Machine_Learning_based_Movie_Recommendation_System)
5. [Additional References](https://www.reddit.com/r/webdev/comments/4649rw/rotten_tomatoes_api/)

---

Thank you for using CinFind!
