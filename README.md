# Heroes vs Villains
## Description of project

Main purpose of Heroes vs Villains project it to classify movie characters into three categories: heroes, villains, and neutral characters based on the words they use. Since I do not have the rights to use actual movie dialogues, I built a character and words generator that creates fictional characters and assigns them words based on predefined distributions.

### Part1. Character and Words Generator

The generator creates a random (but in defined range) number of heroes, villains, and neutral characters. Each Character  receive number of words based on distibution defined to particular group. 

Each character words are defined by four list. Words are unique for particular list and all characters can use words from each list but their usage is limited by character type. For example Hero can use Villains word but their overal usage will be lower that Villains characters. Four predefined word lists are:

* Heroic words
* Villainous words
* Neutral words
* Creative phrases (common to all characters)

Rules for words definition and their distribution is described in notebook. Such approach will ensures a unique dataset for analysis.

### Part 2 Machine learning project

1. Exploratory Data Analysis (EDA)
* The generated dataset is analyzed to identify patterns in word usage across different character types.
* Various word count limits are tested to see how restricting the number of words affects classification score.

2. Feature Engineering and TF-IDF
* The dataset is processed using TF-IDF (Term Frequency-Inverse Document Frequency) to extract meaningful features. 
* Different values of the max_features parameter are tested to optimize classification performance.

3. Classification Models
* The main classification task is to distinguish between heroes, villains and neutral characters. 
* Random Forest is used as basic classifier with pipeline and GridSearch

4. Word Cloud Visualization
* A word cloud is generated to visually represent the most common words used by each character type.

5. Analysis & Findings
* Multiple tests are conducted to find the optimal upper and lower treshold for more robust classification.
* The impact of different TF-IDF settings is analyzed.
* Two detailed summaries present key insights and conclusions from the experiments.

### Why This Project Matters

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
	git clone https://github.com/PiotrPieciak/LEARN_04_SYNTHETIC_Heroes_vs_Villains.git
	cd LEARN_04_SYNTHETIC_Heroes_vs_Villains
 	```
  
3. Create and activate a Conda environment (optional but recommended)
	```
	conda create --name Heroes_vs_Villains python=3.10
	conda activate Heroes_vs_Villains
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
* Open LEARN_04_SYNTHETIC_Heroes_vs_Villains.ipynb in Jupyter Notebook.
* Before you run program you can locate cell after [36] and mark it to stop program execution at this step. It is not neccessary but it will allow you to optimize further analysis based on observation until that point. You can write your own tresholds in cells [39], [41], [43]. 
* Run rest of the cells to execute the analysis.

**Note:**  The picture (Villain 2.png) must be in the folder /img which must be located in the same directory as notebook, to work correctly.

## Dependencies
* matplotlib==3.9.2
* numpy==1.26.4
* pandas==2.2.2
* scikit-learn==1.5.1
* seaborn==0.13.2
* faker==34.0.2
* nltk==3.9.1
* pillow==11.0.0
* wordcloud==1.9.3
