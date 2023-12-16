# deep-learning-challenge

Introduction
Alphabet soup wants to develop a toll using machine learning and neural networks. The goal is to predict the success of funding applicants by analyzing the dataset features. It is a clever way to choose the most promising ventures to fund.
Data Preprocessing
What variable (s) are the target(s) for your model?
The ‘IS_SUCCESSFUL’ column in the application dataset is the one we are interested in. It serves as the target variable and helps us predict whether the funding was used effectively. It’s a crucial factor to consider in selecting the best applicants for funding

The variable(s) are the features of the model these are: -
i.	AFFILIATION—Affiliated sector of industry
ii.	CLASSIFICATION—Government organization classification
iii.	USE_CASE—Use case for funding
iv.	ORGANIZATION—Organization type
v.	STATUS—Active status
vi.	INCOME_AMT—Income classification
vii.	SPECIAL_CONSIDERATIONS—Special considerations for application
viii.	ASK_AMT—Funding amount requested

What variable should be removed from input data because they are neither targets nor features

•	Identification columns: The "EIN" and "NAME" columns are identification columns that typically provide unique identifiers for each organization. These columns usually have no direct impact on the target variable and can be dropped without affecting the model's accuracy.





Compiling, training and evaluating model
My initial neural network model, I opted for a two layer architecture and made specific choices for the number of neurons, layers and activation functions
 

I selected 80 neurons for the first hidden layer (units 1 = 80) and 30 neurons for the second hidden layer (units 1 = 30). To introduce non linearity and capture relationships I used the ReLU activation function (activation = ‘relu’) for both hidden layers/
For the output layer I used a single neuron (units=1) with a sigmoid activation function (activation = ‘sigmoid’) to handle the binary classification problem. The sigmoid function maps the output to a range of 0 to 1, representing the probability of the positive class.
Overall, my model’s architecture, with the specific number of neurons, layers and activation functions aimed to strike a balance between complexity and simplicity. This allows the model to effectively learn and generalize from a given classification task.
Were you able to achieve the target performance?
•	As you can see below, I was only able to achieve 73%.
268/268 - 1s - loss: 0.5753 - accuracy: 0.7266 - 705ms/epoch - 3ms/step
Loss: 0.5753018856048584, Accuracy: 0.7266472578048706





What steps did I take in attempt to increase model performance?

Model: "sequential
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 dense (Dense)               (None, 7)                 3584      
                                                                 
 dense_1 (Dense)             (None, 14)                112       
                                                                 
 dense_2 (Dense)             (None, 1)                 15        
                                                                 
=================================================================
Total params: 3711 (14.50 KB)
Trainable params: 3711 (14.50 KB)
Non-trainable params: 0 (0.00 Byte)


268/268 - 1s - loss: 0.4704 - accuracy: 0.7879 - 608ms/epoch - 2ms/step
Loss: 0.4703502953052521, Accuracy: 0.7878717184066772
Adding more layers in the model can definitely enhance its capacity to capture and represent complex relationship in the data. Each layer can learn different levels of abstraction, allowing model to extract more significant features and potentially boost accuracy. Deep models with multiple layers have the capability to learn hierarchical representations of the data which can really be beneficial for tackling intricate problems.
I was able to achieve 79%

Conclusion
The deep learning model that I have developed was able to achieve accuracy higher than 73%.


References
IRS. Tax Exempt Organization Search Bulk Data Downloads. https://www.irs.gov/Links to an external site.