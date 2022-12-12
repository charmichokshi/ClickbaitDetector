# HeadlineClickbaitDetector

Is that headline Clickbait? is a Transformer-based News Clickbait Detector. It is a Fall 2022 Course Project of COMP599 Natural Language Understanding with Deep Learning at McGill University.
 
To catch readers attention digital and print media are using “Clickbait” headlines. To their monetary benefits, they are misleading the population by publishing catchy headlines to get more user engagements and clicks per post. In this project, we will try to find an answer to a fundamental question that if only a new article’s headline is sufficient to successfully classify if it is clickbait or would we also need more context from related body of the article.

### Instructions for use

The code is present inside the [code](code) folder.

The [process](code/process) folder contains the scripts for data preperation to convert the given jsonl files to a dataframe which inturn is converted to CSV file for further use.

The [classical_ml_approach_headline](code/classical_ml_approach_headline.ipynb) notebook has SVM and XGBoost based approach on the headline of the data.

The [clickbait_classification_headline_article](code/clickbait_classification_headline_article.ipynb) notebook has Clickbait Detection on Headline's text & Article's text using Deberta and Electra pre-trained Models and their Tokenizers.

The [clickbait_classification_headline](code/clickbait_classification_headline.ipynb) notebook has Clickbait Detection on Headline's text using Deberta and Electra pre-trained Models and their Tokenizers.

The [clickbait_classification_headline_thresholding_pr_curve](code/clickbait_classification_headline_thresholding_pr_curve.ipynb) notebook is used for thresholding for electra and deberta and evaluating the PR curve how well the models are classifying.

The [analyse_generated_headline](code/title_generation/analyse_generated_headline.ipynb) notebook in title_generation folder uses SentenceBert to get the embeddings of Ground Truth and Generated headlines. Then it uses similarity metrics and thresholding to evaluate the classification task of clickbait vs non-clickbait.

The [prepare_title_gen_data](code/title_generation/prepare_title_gen_data.ipynb) notebook in title_generation folder is used for preprocessing data to pass it to T5 model.

The [T5 Fine tune and Rouge](code/title_generation/T5%20Fine%20tune%20and%20Rouge.ipynb) notebook in title_generation folder is used for Fine-Tuning T5-base model to current data and uses Rouge score to select the best model.

The [title_generation_T5_fine_tuned](code/title_generation/title_generation_T5_fine_tuned.ipynb) and [title_generation_T5_of_the_shelf](code/title_generation/title_generation_T5_of_the_shelf.ipynb) notebooks in title_generation folder are used to generate headline based on the article text using the the two different models on train and test set of clickbait and no-clickbait samples.

The [visualize_embeddings](code/title_generation/visualize_embeddings.ipynb) notebooks in title_generation folder is used for data visualization like generating TSNE plots.
