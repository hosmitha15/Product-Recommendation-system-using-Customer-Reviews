Product-Recommendation-system-using-Customer-Reviews:
A Product Recommendation System Using Customer Reviews leverages natural language processing (NLP) and machine learning techniques to analyze customer feedback and generate personalized product suggestions. Traditional recommendation systems often rely on structured data, such as purchase history or ratings, but integrating customer reviews provides a deeper understanding of user preferences and product attributes. By extracting sentiment, identifying key themes, and matching user interests to product features, the system delivers tailored recommendations that enhance user satisfaction and engagement. The use of NLP models, such as sentiment analysis and topic modelling, enables the system to interpret unstructured text data effectively. This approach not only improves the accuracy of recommendations but also empowers businesses to understand customer needs and optimize their offerings. The implementation of such a system involves preprocessing customer reviews, feature extraction, and model training to ensure reliable and meaningful outputs. This project explores the development and evaluation of a robust recommendation engine, with potential applications in e-commerce, entertainment, and other sectors where personalized user experiences are paramount. The system demonstrates the transformative potential of combining customer feedback with advanced technologies to deliver value-driven, user-centric solutions.
The detailed stepby step procedure of the project is explained in the form of a flow chart in below figure
![image](https://github.com/user-attachments/assets/aa87507c-d2aa-4c0a-bb3e-f2a7097220db)
Steps involved:
1. Preprocessing:
   i) Load the dataset and search if there are any null values in each column and if any null values are found they are being removed.
   ii) Converting the necessary target and feature data into numeric data for better classifiaction.
   iii) Removing the duplicate values in the dataset.
2. Feature Engineering and Outlier Treatment:
   i) Calculating the total length of the required columns (here length of title column is being calculated)
   ii) Outlier detection and treatment using IQR for 'reviews'.
   iii) Filtering the rows within the IQR range for 'reviews'.
3. Standardization:
   i) Standardized the data using the Stanadard Scaler.
   ii) Implemeted few NLP tasks for the reviews by conversion of whole text into LowerCase, removed the stop words from it, Lemmatization and joined words back 
       into a single string.
4. Splitting of Dataset:
   i) Considering only the stars as the target variable and rest of the columns as faetures, the dataset is being split into test and training dataset.
5. Sentiment Analysis and Helpfullness Ratio:
   i) Calculated Sentiment analysis for 'title' column using a TextBlob (it returns Sentiment score between -1 amd 1)
   ii) Replaced HelpfulnessNumerator and HelpfulnessDenominator with 'reviews' (numerator) and 'stars' (denominator)
   iii) User profiles Aggregation and Product profiles aggregation and displayed them
6. Collaborative Filtering:
   i) Split the dataset into train and test, initialized SVD model, tarined it, made predictions and calcualted RMSE value.
7. Content based filtering using TF-IDF and Cosine Filtering:
   i) Computed Cosine similarity matrix and calculated the similarity score and top 10 similar products have been obtained.
8. Testing:
   i) Tested against a sample valid product title and it suggested a product that is best amongst all similar to sample type.

Language used: Python
Python libraries used: pandas, matplotlib, seaborn, scikit-learn, TextBlob, Surprise
NLP libraries used: NLTK

