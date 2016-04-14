# EnronDataAnalysis

<h1>Enron Data Analysis with AdaBoost and SelectFromModel</h1>

The Enron email corpus is one of the most famous in data science and machine learning. My investigation of the features provided by Udacity's ML Final Project was an attempt to sift out meaningful trends and, notably, to achieve precision and recall scores above 0.3 -- this report will detail my process, results and commandline output towards those goals.

<h1>Conclusion</h1>
Using a StratifiedShuffleSplit dataset with 0.05 testing set proportionally, the highest accuracy, precision, recall and f1 scores I was able to obtain were, respectively, <b>0.85</b>, <b>0.42</b>, <b>0.33</b>, and <b>0.37</b>. This was achieved using the features <b>bonus</b>, <b>total_stock_value</b>, <b>expenses</b>, <b>exercised_stock_options</b>, <b>other</b>, and <b>shared_receipt_with_poi</b>, selected via SelectFromModel. My AdaBoostClassifier was tuned to <b>learning_rate = 0.3</b> and <b>n_estimators = 100</b>.</p><p>What this means for my program is that 85% of the time, I correctly guessed the POI status of an individual. Of the people I guessed who were POI's, I got 42% of them right, and of all the POI's, I spotted 33% of them. This definitely meets the project requirments, and I'd say isn't a bad performance for such a nuanced dataset.</p><p>Next steps I would take for this project would be to compare a more complex sentiment map of the email corpus; maybe devise some features exploring how many emails about money, or about deals, were sent or recieved by POI status. Another would be to pull dates out from the emails, and see the rate at which POIs sent emails during certain periods associated with the start of specific fraudulent acts.
