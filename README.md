# predict-healthcare-costs
Predicting healthcare costs using Keras.

### Data
The project uses the health insurance dataset, which can be downloaded using the following command:  <br>
`!wget https://cdn.freecodecamp.org/project-data/health-costs/insurance.csv'`
### Data preprocessing
Before training the machine learning model, some preprocessing steps are performed on the dataset: <br>
* Mapping the 'sex' column values to binary values (0 for female, 1 for male).
* Mapping the 'smoker' column values to binary values (0 for no, 1 for yes).
* Encoding the 'region' column using factorization.
The dataset is then split into training and test datasets, with 80% of the data used for training and 20% for testing.

### Model Architecture
The machine learning model is implemented using a sequential model from Keras. The model architecture consists of the following layers:
<br>
* Normalization layer: Normalizes the input features.
* Dense layer with 16 units.
* Dense layer with 4 units.
* Dropout layer with a dropout rate of 0.2.
* Dense output layer with 1 unit. <br>
The model is compiled with the Adam optimizer using a learning rate of 0.1 and the mean absolute error (MAE) as the loss function. The metrics used for evaluation are MAE and mean squared error (MSE).
