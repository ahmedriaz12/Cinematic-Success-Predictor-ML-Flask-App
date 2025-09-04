# Cinematic Success Predictor

We explored ten years of movie data, trained a machine learning model, and built a Flask web app to forecast whether a new film is likely to succeed or flop. By entering details such as budget, runtime, director, cast, or even a short plot, the app predicts the movie’s chances of success with ~71% accuracy.  

---

### Goals
- Build a supervised ML model to forecast potential movie ratings.  
- Perform historical trend analysis using a decade of movie data.  
- Deliver an interactive web app with predictions and visualization dashboards.  

---

### ETL Workflow
- **Extract**: Retrieve movie datasets from OMDb via API calls, grouped by year.  
- **Transform**: Clean with Pandas—merge dataframes, handle nulls (`NA`/`0`), deduplicate, and normalize headers.  
- **Load**: Export the final dataset into CSV and store in SQL for analysis.  

---

### Exploratory Insights
Using Python (Pandas, Matplotlib, Seaborn, WordCloud), we uncovered:  
1. IMDb critic ratings and user votes show weak correlation.  
2. Budget and IMDb rating have little direct link.  
3. Budget and box office gross are strongly correlated.  
4. Rotten Tomatoes and Metascore often reflect differing opinions on the same film.  

---

### Data Preprocessing
- Labeled movies based on IMDb scores.  
- Selected predictive columns (runtime, budget, cast, director, etc.).  
- Converted categorical data to numeric (One-Hot Encoding, `get_dummies`).  
- Consolidated rare values across country, language, and genre.  
- Grouped IMDb ratings into bins: `<5`, `5–7`, `>7`.  
- Vectorized movie plot text for NLP integration.  
- Combined all features into a unified dataset.  

---

### Modeling
We applied a Random Forest Classifier.  
The main hurdle was incorporating plot summaries—resolved through multi-step NLP preprocessing to represent text as meaningful vectors for training.  

---

### App Deployment
A Flask app hosts:  
- An interactive dashboard showing data relationships.  
- A prediction tool merging vectorized plots with other features to generate success probability.  

[View Our Presentation](https://docs.google.com/presentation/d/1pIVyzZgfz74ZjjOsThbbvJReoxf9x3Ym12RAgRuAm8w/edit#slide=id.g112884da369_0_405)  

---

### Resources
- [OMDb API](http://www.omdbapi.com)  
- [Kaggle Movies Dataset](https://www.kaggle.com/danielgrijalvas/movies)  

---

- [Maria DiPasquale](https://github.com/edipasq)  
- [Daniel Kletter](https://github.com/dkletter)  
