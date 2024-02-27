# Charity_Use_Case_Challenge



The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With  knowledge of machine learning and neural networks, I'm using the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.


First step is preparing the data: 

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

    EIN and NAME—Identification columns
    APPLICATION_TYPE—Alphabet Soup application type
    AFFILIATION—Affiliated sector of industry
    CLASSIFICATION—Government organization classification
    USE_CASE—Use case for funding
    ORGANIZATION—Organization type
    STATUS—Active status
    INCOME_AMT—Income classification
    SPECIAL_CONSIDERATIONS—Special considerations for application
    ASK_AMT—Funding amount requested
    IS_SUCCESSFUL—Was the money used effectively

Shown below is the number of values found in each of the columns: 

![Screenshot 2024-02-26 at 9 25 18 PM](https://github.com/davisdw/Charity_Use_Case_Challenge/assets/104311388/c88806fa-cccd-4fda-9857-1179c5299a80)


Next is to create binning for values that is considerable small outliers and have them group and assign as Other category: In this case Application Type and Classification is utilized 

![Screenshot 2024-02-26 at 9 26 25 PM](https://github.com/davisdw/Charity_Use_Case_Challenge/assets/104311388/6bfc420f-bc96-4a0d-b6fc-b57616bd36e2)



![Screenshot 2024-02-26 at 9 27 12 PM](https://github.com/davisdw/Charity_Use_Case_Challenge/assets/104311388/da282874-366c-40a2-87cf-8a962edfa953)


Afterwards Split the feature and target dataset by removing the IS_SUCCESSFUL Column and assign it to an different variable called "y" while taking the remaining data and assigning to "X"

Next step is creating an split train test model dataset and using scalar to fit the dataset


Next Step is Compiled Train and Test the Model to determine if the company has successful outcome 

Using the choice of the following is using the keras model (for neural networking) and designed the following parameters: 

    # Define the model - deep neural net, i.e., the number of input features and hidden nodes for each layer.
      number_input_features = len(X_train_scaled[0])
    
    # Hidden layers = 3 each layer incremented by 7
      hidden_nodes_layer1 = 7
      hidden_nodes_layer2 = 14
      hidden_nodes_layer3 = 21
    
      nn_model = tf.keras.models.Sequential()
      

![Screenshot 2024-02-26 at 9 28 25 PM](https://github.com/davisdw/Charity_Use_Case_Challenge/assets/104311388/8b4938ff-69e6-4e2b-acac-1ab9abf26660)


After running the model test to determine the acuuracy was approriate I've ran the the Test model and results as shown 

![Screenshot 2024-02-26 at 9 28 48 PM](https://github.com/davisdw/Charity_Use_Case_Challenge/assets/104311388/f3ca363e-c073-4a5f-8ffb-07f3630e08a2)

Results shown with model accuracy of 74% which indicated that the accuracy of the company's successful rate with 55% of loss

