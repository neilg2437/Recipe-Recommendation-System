# Recipe-Recommendation-System

🚀 Recipe Recommendation System using NLP & GPT-2
📌 Project Overview
This project builds an NLP-powered recipe recommendation system that suggests recipes based on user inputs. The system:
✅ Uses GPT-2 from Hugging Face for text generation.
✅ Collects 775 recipes across 20 cuisines using the Tasty API.
✅ Applies NLP techniques (TF-IDF, Named Entity Recognition, and Prompt Engineering) to improve recommendations.

🛠️ Technologies Used
Python (Data Processing & Model Implementation)
Hugging Face GPT-2 (Pre-trained NLP Model)
NLTK & SpaCy (Text Preprocessing & Named Entity Recognition)
TF-IDF & Cosine Similarity (Ranking Relevant Recipes)
Tasty API (Recipe Data Collection)
Pandas & NumPy (Data Handling & Feature Engineering)
📂 Dataset & Data Preprocessing
Data Source: Collected from Tasty API (free and public).
Dataset: Contains 775 recipes across 20 cuisines.
Storage: Recipes stored in an Excel file, loaded into a pandas DataFrame for reproducibility.
🔹 NLP Preprocessing Steps
1️⃣ Data Cleaning (Lowercasing, Tokenization, Stopword Removal, Lemmatization) using NLTK.
2️⃣ Tag Standardization (Converting cuisine labels for consistency).
3️⃣ Named Entity Recognition (NER): Identifies key food ingredients & cuisine types.
4️⃣ TF-IDF Vectorization: Converts text into numerical form for similarity ranking.
5️⃣ Prompt Engineering: Guides GPT-2 to generate structured responses.

🔍 How the Model Works
1️⃣ User Input Processing
User enters a prompt like:
"Give me a Mexican recipe with chicken."
Preprocessing removes noise & extracts keywords (NER-based filtering).
2️⃣ Recipe Matching with TF-IDF
The system converts recipe descriptions into TF-IDF vectors.
Cosine similarity measures how closely a recipe matches user input.
3️⃣ Boosting with Named Entity Recognition (NER)
Certain keywords (e.g., "chicken," "Mexican") receive higher weights.
Recipes with matching cuisine & ingredients are prioritized.
4️⃣ GPT-2 for Final Refinement
Prompt Engineering improves the recipe suggestions.
Uses few-shot learning with example prompts to refine outputs.
📊 Example Recommendation Flow
🔹 User Input: "Give me a Mexican recipe with chicken."
🔹 Recipe Descriptions:
1️⃣ "This is a Mexican taco recipe with chicken."
2️⃣ "This is a Mexican beef stew."

Word	User Input	Recipe 1 (Taco)	Recipe 2 (Stew)
Mexican	High	High	High
Chicken	High	High	Low
🔹 Similarity Score Calculation:

Recipe 1 Score: 0.85 (TF-IDF) + 0.12 (Mexican boost) + 0.10 (Chicken boost) = 1.07 ✅
Recipe 2 Score: 0.75 (TF-IDF) + 0.12 (Mexican boost) = 0.87
🛠️ Final Recommendation: Mexican Taco Recipe with Chicken

📌 Model Architecture
A visual representation of the workflow & model pipeline:
(🔽 Architecture diagram will be generated next.)

📌 How to Run This Project
1️⃣ Install Dependencies
sh
Copy
Edit
pip install transformers pandas numpy nltk spacy scikit-learn
python -m spacy download en_core_web_sm
2️⃣ Run the Recipe Recommendation System
sh
Copy
Edit
python recipe_recommendation.py
3️⃣ Sample Input & Output
User Input:

sh
Copy
Edit
Give me a Thai recipe with shrimp.
Expected Output:

sh
Copy
Edit
"Try this delicious Thai shrimp stir-fry with a tangy lime sauce!"
🎯 Key Results & Observations
✅ Understands cuisine types well.
✅ Provides relevant recipe suggestions.
❌ Ingredient matching can be improved.
✅ Fine-tuned prompt engineering helped refine responses.

