# Final Project: Sentiment Analysis and Ethical AI Concerns

## Introduction
This project analyzes sentiment in tweets using the Sentiment140 dataset while incorporating ethical AI concerns such as fairness, transparency, privacy, and accountability. Through sentiment analysis and ethical keyword mapping, the project provides insights into public opinions on these critical AI topics.

## Dataset
- **Name**: Sentiment140 Dataset
- **Description**: A dataset of 1.6 million tweets annotated for sentiment analysis.
- **Columns**:
  - `sentiment`: Sentiment of the tweet (0 = negative, 4 = positive).
  - `tweet_id`: Unique identifier for the tweet.
  - `timestamp`: Date and time of the tweet.
  - `query`: Query used to search for the tweet.
  - `user`: Username of the account.
  - `text`: Text content of the tweet.
- **Size**: Approximately 227 MB.

## Methodology
1. **Data Cleaning**:
   - Removed mentions (e.g., `@username`).
   - Removed URLs.
   - Removed special characters and converted text to lowercase.
   - Example function:
     ```python
     def clean_tweet(text):
         text = re.sub(r'@\w+', '', text)  # Remove mentions
         text = re.sub(r'http\S+|www\S+', '', text)  # Remove URLs
         text = re.sub(r'[^A-Za-z0-9\s]+', '', text)  # Remove special characters
         return text.lower().strip()
     ```

2. **Sentiment Analysis**:
   - Used the Sentiment140 sentiment annotations for initial analysis.
   - Implemented **VADER Sentiment Analysis** for more nuanced scoring.
     - **Metrics**: Positive, Neutral, Negative, and Compound Score.

3. **Ethical Concerns Categorization**:
   - Keywords were mapped to ethical categories:
     - **Fairness**: `bias`, `discrimination`.
     - **Transparency**: `explainability`, `clarity`.
     - **Privacy**: `confidentiality`, `data protection`.
     - **Accountability**: `responsibility`, `ownership`.
   - Tweets were tagged with relevant categories based on keyword matches.

4. **Visualizations**:
   - **Sentiment Distribution**:
     - Bar charts of positive and negative tweets.
     - Example:
       ![Sentiment Distribution](#)
   - **Word Clouds**:
     - Positive and negative word clouds to highlight common themes.
       ![Word Cloud](#)
   - **Trends Over Time**:
     - Line graphs showing trends in ethical concerns over months.

## Results
- **Sentiment Distribution**:
  - The dataset shows a balanced distribution of positive and negative tweets.
- **Ethical Categories**:
  - `Bias` and `Privacy` were the most commonly discussed concerns.
  - Sentiment within these categories indicated mixed opinions on ethical issues.
- **Trends**:
  - Public concern for `Transparency` and `Accountability` increased during specific time periods.

## Technologies Used
- **Programming Language**: Python
- **Libraries**:
  - `pandas`: Data manipulation.
  - `numpy`: Numerical computations.
  - `matplotlib` & `seaborn`: Data visualization.
  - `vaderSentiment`: Sentiment analysis.
  - `wordcloud`: Word cloud generation.
  - `scikit-learn`: Machine learning (if applicable).

## Usage
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/SaimAkramGill/fcss_project.git
   cd fcss_project
   ```

2. **Install Requirements**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Analysis**:
   - Preprocessing and Sentiment Analysis:
     ```bash
     python analysis.py
     ```
   - Visualizations:
     ```bash
     python visualizations.py
     ```

4. **View Results**:
   - Outputs (e.g., graphs, cleaned data) will be saved in the `/results` folder.

## Conclusion
This project demonstrates the power of sentiment analysis combined with ethical AI concerns. By analyzing public opinion, it highlights key areas of concern and discussion around AI ethics. Future work could incorporate real-time data streams and advanced NLP models for deeper analysis.

## Future Enhancements
- Incorporate real-time tweet analysis using Twitter's API.
- Expand ethical categories with more nuanced definitions.
- Experiment with advanced machine learning models like BERT for sentiment classification.

---

### Contact
For any questions or contributions, please contact **Saim Akram** at saimakram41@gmail.com.
