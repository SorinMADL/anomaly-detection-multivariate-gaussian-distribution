# anomaly-detection-multivariate-gaussian-distribution
anomaly detect. with MVGaussian Distrib
(dataset:https://www.kaggle.com/mlg-ulb/creditcardfraud)



For first, i normalize the dataset, and cuz i got i large dataset, I did a split 99% for train, 2% for dev set.
Then, with function estimateGaussian I got the miu and sigma for the dataset, and for prediction i used the multivariate Gaussian (cuz even is more computional exepsiv, offers a better prediction).
Now having the prediction is time to choose the epsilon, the factor that tell u if a given example is anomalous or not.
The function to select the treshold (select_the_treshold), got 2 extra params, 'an' - who penalize de F1 score if an anomaly wasn t identif. corectly (more exactly ,this one penalize the 'false negative'), and 'nonan' - who penalize de F1 score when target a non anomaly as anomaly(more exactly ,this one penalize the 'false positive').

The default result for this dataset was:
 - for training set: 
        ACC: 99.43%  |  how meny abnormalities we got from the total of abnormalities: 44.35 % | from total of abnormalities: 487 we got: 216 | how meny non abnormalities we targeted as abnormalities: 1304 from total of non abnormalities: 278624 (0.46%)
        
 - for training dev set: 
        ACC: 99.52%  |  how meny abnormalities we got from the total of abnormalities: 40.00 % | from total of abnormalities: 5 we got: 2 | how meny non abnormalities we targeted as abnormalities: 24 from total of non abnormalities: 5691 (0.42%)
        
