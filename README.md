# Heroes vs Villains
## Description of project

The Heroes vs. Villains project main purpose it to classify movie characters into three categories: heroes, villains, and neutral characters based on the words they use. Since I do not have the rights to use actual movie dialogues, I built a character and words generator that creates fictional characters and assigns them words based on predefined distributions.

Part1. Character and Speech Generator
        The generator creates a random (but in defined range) number of heroes, villains, and neutral characters.
        Each character is assigned words from four predefined word lists:
            Heroic words
            Villainous words
            Neutral words
            Creative phrases (common to all characters)
        This ensures a unique dataset for analysis.

    Exploratory Data Analysis (EDA)
        The generated dataset is analyzed to identify patterns in word usage across different character types.
        Various word count limits are tested to see how restricting the number of words affects classification accuracy.

    Feature Engineering and TF-IDF
        The dataset is processed using TF-IDF (Term Frequency-Inverse Document Frequency) to extract meaningful features.
        Different values of the Max Features parameter are tested to optimize classification performance.

    Classification Models
        The main classification task is binary classification: distinguishing between heroes and villains.
        Various classification models are tested to determine the most effective approach.

    Word Cloud Visualization
        A word cloud is generated to visually represent the most common words used by each character type.

    Analysis & Findings
        Multiple tests are conducted to find the optimal upper and lower word count limits for accurate classification.
        The impact of different TF-IDF settings is analyzed.
        Two detailed summaries present key insights and conclusions from the experiments.

Why This Project Matters

This project explores how language influences perception and how simple word choices can define a character as heroic, villainous, or neutral. By generating synthetic data and applying machine learning techniques, it demonstrates a creative approach to text classification in the absence of real-world datasets.

Check out the full project, experiments, and insights in the repository!

## Dataset 
The dataset used is this project is fully sythetic and created by my own generator. All pictures used in this project are AI generated and modified by myself. 

Any similarities to real films and characters are coincidental and not intentional.

## Installation & Setup
To run this project, you need **Python** and **Jupyter Notebook** installed and the required libraries. Follow these steps using **Anaconda Prompt**:

1. Download the repository
Click on the **Code** button and select **Download ZIP** or clone the repository using Git:	
 	```
	git clone .git
	cd LEARN_02_KODILLA_Credit_Card
 	```
  
3. Create and activate a Conda environment (optional but recommended)
	```
	conda create --name Credit_Card python=3.10
	conda activate Credit_Card
	```
 
4. Instal required dependencies:
	```
	pip install -r requirements.txt
 	```
 
5. Open Jupyter Notebook:
	```
 	jupyter notebook
  	```
 
6. Run the project
* Open LEARN_02_KODILLA_Credit_Card_Defaulter_Prediction.ipynb in Jupyter Notebook.
* Run all cells to execute the analysis.

**Note:**  The dataset (default_of_credit_card_clients.xls) must be in the same folder as the notebook for the code to work correctly.

## Dependencies
matplotlib==3.9.2
numpy==1.26.4
pandas==2.2.2
scikit-learn==1.5.1
seaborn==0.13.2
faker==34.0.2
nltk==3.9.1
pillow==11.0.0
wordcloud==1.9.3
