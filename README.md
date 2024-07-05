# House Price Prediction

This project implements a linear regression model to predict house prices based on their square footage, the number of bedrooms, and the number of bathrooms. The model is trained using a dataset of house features and prices, and predictions are made on a test dataset.

## Files in the Repository

- `train.csv`: Training dataset containing house features and prices.
- `test.csv`: Test dataset containing house features (without prices).
- `predict_house_prices.py`: Python script to train the model and make predictions.
- `test_predictions.csv`: Output file containing the predicted house prices.

## Steps to Run the Project

### 1. Load the Data
The data is loaded from the provided CSV files using pandas.

### 2. Select Relevant Features
The relevant features for the model are selected:
- `GrLivArea` (above ground living area square footage)
- `BedroomAbvGr` (number of bedrooms above ground)
- `FullBath` (number of full bathrooms)

The target variable is `SalePrice`.

### 3. Handle Missing Values
Any missing values in the selected features are filled with the median value of the respective column.

### 4. Split the Data
The training data is split into training and validation sets to evaluate the model's performance.

### 5. Train the Linear Regression Model
A linear regression model is trained using the training data.

### 6. Evaluate the Model
The model's performance is evaluated on the validation set using Root Mean Squared Error (RMSE).

### 7. Make Predictions on the Test Data
The test data is preprocessed in the same way as the training data, and predictions are made using the trained model.

### 8. Save Predictions to CSV
The predictions are saved to a new CSV file (`test_predictions.csv`).

## Usage

To run the project, follow these steps:

1. Make sure you have Python installed on your system.
2. Install the required libraries using pip:
    ```bash
    pip install pandas scikit-learn
    ```
3. Run the Python script `predict_house_prices.py`:
    ```bash
    python predict_house_prices.py
    ```

This will generate the `test_predictions.csv` file with the predicted house prices.

## Model Performance

The RMSE on the validation set is approximately 52975.72, indicating the average deviation of the predicted house prices from the actual prices.

## License

This project is licensed under the MIT License.
