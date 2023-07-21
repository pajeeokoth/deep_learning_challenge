# deep_learning_challenge
Deep Learning and Neural Networks
1.  Overview of the analysis: Explain the purpose of this analysis.
We will use neural networks and machine learning to analyze data from The nonprofit foundation Alphabet Soup and develop a tool to help them select applicants for funding with the best chance of success in their ventures. We will use a binary classifier to to predict whether an applicant will be successful if funded by Alphabet Soup.

2.  We will address the following questions in our analysis:

    ##    Data Preprocessing

- What variable(s) are the target(s) for your model?
For the neural network model the model target is whether a funding venture was previously successul or unsuccessul (IS_SUCCESSFUL)

- What variable(s) are the features for your model?
All the other variables are the features for the model.
What variable(s) should be removed from the input data because they are neither targets nor features?
            EIN and NAME—Identification columns
            APPLICATION_TYPE—Alphabet Soup application type
            AFFILIATION—Affiliated sector of industry
            CLASSIFICATION—Government organization classification
            USE_CASE—Use case for funding
            ORGANIZATION—Organization type
            STATUS—Active status
            INCOME_AMT—Income classification
            SPECIAL_CONSIDERATIONS—Special considerations for application
            ASK_AMT—Funding amount requested.

- Compiling, Training, and Evaluating the Model
Using the tensorflow package and pyspark, data was split into training and testing sets, initialised the neural network, compiled the model and used model accuracy and loss to evaluate the model,.

3.  How many neurons, layers, and activation functions did you select for your neural network model, and why?
To start, the model was fit with two hidden layers each with 80 and 30 neurons respectively with relu activation function, with one output layer with a sigmoid activation function. These were random choices. An accuracy of about 74% was achieved.

- Were you able to achieve the target model performance?
The model performance was not achieved as required to be more than 75%, our models and attempted improvements only managed to achieve an accuracy of about 74%.

- What steps did you take in your attempts to increase model performance?
In order to improve on the accuracy we tweaked the model, first by collasping some of the features and adding another hidden layer, these tweaks did not result in any model performance improvent. 
We also tried to drop some features that seemed redudant, this did not result in model performance improvement but performance ended up detriorating to an accuracy of about 70%.Using auto hyperparameter tuning did not result in a more improved model.

4.  Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation. 
From model trained and tested, the best model had two hidden layers with (80 and 30) neurons and was able to achieve accuracy score of 74%. from this we can trust the model that in the long run it can correctly identify projects to fund that would be successful about 74% of the time. This is not a perfect score but it is good enough to ensure that the company can limit funds to unsussful project and frequently fund successful projects.