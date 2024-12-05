Here is an extensive `README.md` draft covering both directories:

---

# Data Science Projects

This repository contains two main projects: one focused on Airbnb data analysis in Athens and another that examines the effectiveness of nonviolent vs. violent campaigns. Each project is self-contained in its respective directory and includes data, scripts, and documentation.

## Table of Contents
- [Project 1: Airbnb Analysis in Athens](#project-1-airbnb-analysis-in-athens)
  - [Objectives](#objectives)
  - [Directory Structure](#directory-structure-1)
  - [Results](#results-1)
- [Project 2: Violent vs. Nonviolent Campaigns](#project-2-violent-vs-nonviolent-campaigns)
  - [Objectives](#objectives-2)
  - [Directory Structure](#directory-structure-2)
  - [Results](#results-2)
- [Project 3: Spotify Valence](#project-3-spotify-valence)
  - [Objectives](#objectives-3)
  - [Data Sources](#data-sources)
  - [Methodology](#methodology)
  - [How to Run](#how-to-run)
  - [Results and Analysis](#results-and-analysis)
  - [Additional Notes](#additional-notes)
- [Environment Setup](#environment-setup)

---

## Project 1: Airbnb Analysis in Athens

This project explores Airbnb listings in Athens. The goal is to perform exploratory data analysis (EDA) and complete a set of tasks to gain insights into the short-term rental market.

### Objectives
- Analyze the distribution of Airbnb listings across different neighborhoods.
- Study price trends and their relationship to various factors like property type and availability.
- Evaluate the performance of hosts and identify factors that impact ratings and reviews.
- Perform tasks such as data cleaning, feature engineering, and visualizations to summarize findings.

### Directory Structure
```
/datascience/
│── csv files/             # Raw and processed data files (Airbnb dataset)
│── notebooks/             # Jupyter notebooks for EDA and analysis          
```

### How to Run
1. Install the necessary Python packages listed in the `requirements.txt` file.
2. Download the Airbnb dataset (if not already present) and place it in the `data/` directory.
3. Open the Jupyter notebooks under `notebooks/` to follow the analysis and run the EDA tasks.

```bash
pip install -r requirements.txt
jupyter notebook notebooks/eda_airbnb_athens.ipynb
```

### Results
- The analysis provides insights into popular neighborhoods, average listing prices, and the impact of amenities and other features on price.
- Visualizations include price distribution maps and trend graphs for property ratings over time.

---

## Project 2: Violent vs. Nonviolent Campaigns

This project examines the effectiveness of violent and nonviolent campaigns. The research question focuses on whether nonviolent campaigns lead to more successful outcomes than violent campaigns.

### Objectives
- Collect and preprocess data on various violent and nonviolent campaigns.
- Analyze key metrics such as success rates, duration, and participation levels.
- Compare the effectiveness of both types of campaigns using statistical and machine learning methods.

### Directory Structure
```
/viol-nonviol/
│── csv files and figures/                  # Raw and cleaned data on campaigns
│── notebooks/             # Jupyter notebooks for statistical analysis
```

### Results
- The analysis demonstrates that nonviolent campaigns are more likely to succeed than violent campaigns, though there are notable exceptions.
- Machine learning models predict campaign outcomes with a certain level of accuracy based on features such as duration, scale, and type of support.

---

## Project 3 : Spotify Valence

The *valence* metric quantifies the happiness of a track, and understanding its derivation can provide insights into how music characteristics correlate with perceived mood. This project investigates how valence is calculated and proposes a model based on available data and information.

### Objectives

1. **Understand the Valence Metric**: Analyze the information provided by Echo Nest and Spotify to reverse-engineer the valence calculation.
2. **Analyze Audio Features**: Use Spotify's audio features and audio analysis endpoints to gather data and identify patterns related to valence.
3. **Develop a Model**: Propose a model to calculate valence based on the available data and compare it to Spotify’s reported values.
4. **Evaluate Model Performance**: Rank the model using Mean Average Error (MAE) against a test dataset.

### Data Sources

1. **Spotify API**:
   - [Get Track's Audio Features](https://developer.spotify.com/documentation/web-api/reference/#/operations/get-audio-features)
   - [Get Tracks' Audio Features](https://developer.spotify.com/documentation/web-api/reference/#/operations/get-several-audio-features)
   - [Get Track's Audio Analysis](https://developer.spotify.com/documentation/web-api/reference/#/operations/get-audio-analysis)

2. **Zenodo Dataset**: Spotify charts data available at [Zenodo](https://doi.org/10.5281/zenodo.4778562).

3. **Additional Data**: Supplementary datasets or features may be used to enhance the analysis.

### Methodology

1. **Data Collection**:
   - Extract audio features and analysis data from Spotify’s API for a diverse set of tracks.
   - Download and preprocess the Spotify charts dataset from Zenodo.

2. **Feature Analysis**:
   - Investigate the relationship between valence and various audio features such as danceability, energy, tempo, and others.

3. **Model Development**:
   - Develop and test hypotheses on how valence might be derived from the available audio features.
   - Create a predictive model to estimate valence based on these features.

4. **Evaluation**:
   - Use Mean Average Error (MAE) to assess the accuracy of the proposed model.
   - Rank the model based on performance metrics and provide a comparative analysis.

### How to Run

1. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

2. **Run the Analysis**:
   - Download the datasets and place them in the `data/` directory.
   - Execute the provided Jupyter notebooks or Python scripts to perform the analysis and model training.

   ```bash
   jupyter notebook notebooks/valence_analysis.ipynb
   ```

3. **Evaluate the Model**:
   - Test the model with the provided test dataset to calculate MAE and assess performance.

### Results and Analysis

- Summarize the findings from the analysis of valence and its relationship with audio features.
- Present the performance of the proposed model, including MAE metrics and comparative results.

### Additional Notes

- The project will contribute to the understanding of how Spotify measures valence and can potentially improve the accuracy of mood predictions in music.
- Further research may include refining the model with additional data or exploring alternative features.


## Environment Setup

Both projects rely on Python and several external libraries. The following steps outline how to set up the environment:

1. Ensure you have Python 3.7+ installed on your system.
2. Create a virtual environment for the projects:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```
3. (Optional) Install Jupyter if you plan to run the notebooks:
   ```bash
   pip install jupyter
   ```

---

Feel free to adjust the contents as needed and add specific details about your implementation, results, or any additional sections relevant to your project.

