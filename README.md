# credit-risk-classification
<h2>Background</h2>
<p>In this challenge, one of the machine learning models, Logistic Regression, was used to train and evaluate loan risk from a dataset of historical lending activity, in order to identify the creditworthiness of borrowers.</p>
<h2>Technical</h2>
<p>The analysis was conducted through the following steps:</p>
<ul>
<li>Data was read and then split into training and testing sets using <code>train_test_split</code></li>
<li>The training data was fit using a logistic regression model, and the test data was used to predict the data with the fitted model</li>
<li>The model's performance was evaluated by generating a confusion matrix and a classification report</li>
<li>The same dataset was resampled using the <code>RandomOverSampler</code> module to rebalance classification distribution; then the model was fitted using the logistic regression model for evaluation of its performance</li>
<li>A credit risk analysis report was included to summarize the performance of the machine learning models in file named <code>analysis_report.md</code></li>
</ul>