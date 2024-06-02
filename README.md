
# SMS Fraud Detection

This project is aimed at detecting fraudulent SMS messages using machine learning algorithms. The system takes an input SMS message and predicts whether it's spam (fraudulent) or ham (legitimate).

## Libraries Used
- Flask: Web framework used for creating the RESTful API.
- pandas: Library for data manipulation and analysis.
- scikit-learn: Machine learning library for training classifiers and vectorizing text data.
- numpy: Numerical computing library.
- beautifulsoup4: Library for parsing HTML and XML documents.
- scipy: Library for scientific computing.

## Methodology

### Training and Testing
1. **Data Loading**: The project utilizes a dataset (`spam.csv`) containing SMS messages labeled as spam or ham.
2. **Model Training**: Three different scripts (`app.py`, `classifier.py`, `scikit.py`) train various classifiers using different vectorization methods.
   - `app.py`: Uses a Support Vector Machine (SVM) classifier with Term Frequency-Inverse Document Frequency (TF-IDF) vectorization.
   - `classifier.py`: Trains multiple classifiers with different vectorization methods such as CountVectorizer, TF-IDF, and HashingVectorizer.
   - `scikit.py`: Trains an SVM classifier with TF-IDF vectorization.
3. **Model Evaluation**: The performance of each model is evaluated using test data to determine the accuracy of the predictions.

### Deployment
- The `app.py` script sets up a Flask web server to expose a RESTful API endpoint for predicting whether a given SMS message is spam or ham.
- The API endpoint accepts an SMS message as input and returns the prediction along with the probability of the prediction.

## How to Run

1. **Install Dependencies**: Ensure you have Python installed, then run the following command to install required libraries:
   ```
   pip install -r requirements.txt
   ```

2. **Training the Models**: Run the following commands to train the models:
   ```
   python classifier.py
   python scikit.py
   ```

3. **Running the Flask App**: Execute the following command to start the Flask web server:
   ```
   python app.py
   ```

4. **Accessing the API**: Once the server is running, you can access the API endpoint using a tool like Postman or by sending a request to `http://localhost:5000/` with the message parameter.

## Contributors
- Sai Sribhashyam `https://www.github.com/saiSribhashyam`
<!-- 
## License
[License information, if applicable] -->
