# [Air Quality Data Web Application with Django](https://github.com/jwchoi622/aqproj)

## Overview
This project is a Django-based web application designed to provide up to date air quality information for any city in the world. I used the AQICN API to get the air quality data and Leaflet to get the map on the website. Lastly I used PythonAnywhere to deploy the application. The application is accessible at [https://jwchoi622.pythonanywhere.com](https://jwchoi622.pythonanywhere.com). 
## Features
- **Air Quality Information:** The first table will give the current air quality information for the city that the user inputs. It also includes a widget 
  that has a concise summary of current air quality for that city. Not all cities will get a widget because the API seems to only return a widget for major cities. 
  It also may not have information on all of the different types of pollutants such as CO or O3. 
- **Interactive Map:** The map will be centered on the queried city and also have tiles that indicate the AQI index for different neighborhoods within the city. 
  Smaller cities may not have as many tiles because they do not have as many air quality sensors. The user can also zoom in or zoom out to look at neighboring cities. 
- **PM 2.5 Forecast:** The forecast focuses on PM 2.5 because it is the most harmful of pollutants and also a big problem in Korea. The forecast will usually show 
  the PM 2.5 forecast for the next couple days in the week and have color coded dates according to the average level for that date. 
- **Calendar:** The calendar will indicate which days are safe for outdoor activity by looking at the PM 2.5 index. 

## Future Improvements
- Adding a forecast for PM10 would also be helpful in determining what the air quality would be like for future days.
- The calendar could also include markers for good, average and poor air quality.
- Including different language options.

## External APIs Used
### AQICN API
- **Description:** I used this AQICN to get the air quality data, widget, forecast data and also the map tiles.
- **Documentation:** [https://aqicn.org/api/](https://aqicn.org/api/)

### Leaflet API
- **Description:** I used the Leaflet API to get an interactive map of the queried city.
- **Documentation:** [https://leafletjs.com/reference.html](https://leafletjs.com/reference.html)

### OpenCage Geocoding API
- **Description:** I used the OpenCage API to get the latitude and longitude of the city and fed those coordinates into the Leaflet map. 
- **Documentation:** [https://opencagedata.com/api](https://opencagedata.com/api)



# [UFC Fighter Image Classification](https://github.com/jwchoi622/fighterClassification)
* The 5 fighters used were Conor McGregor, Jon Jones, Sean O'Malley, Chael Sonnen and Daniel Cormier

* **Deep Learning Framework:** Developed a deep learning model using the Keras library with TensorFlow backend, demonstrating proficiency in deep learning techniques.

* **Data Preprocessing:** Utilized image data preprocessing techniques, including data augmentation with ImageDataGenerator, and normalized pixel values to enhance model accuracy.

* **Model Architecture:** Constructed a Convolutional Neural Network (CNN) with multiple convolutional layers, max-pooling layers, and fully connected layers, showcasing expertise in neural network architecture design.

* **Performance Evaluation:** Trained and evaluated the model over 20 epochs, monitoring training and validation accuracy and loss, demonstrating the ability to assess model performance and optimize hyperparameters.

* **Visualization:** Visualized the training process by plotting training and validation accuracy and loss, allowing for clear and insightful analysis of model training results.

* **Model Persistence:** Stored the mapping of face classes and their corresponding IDs using Python's pickle library, highlighting data management skills.

* **Project Documentation:** Demonstrated proficiency in documenting and explaining the project steps, from data preprocessing to model architecture, in a clear and organized manner.
![](/images/fightergraph.png)

# [House Price Regression](https://github.com/jwchoi622/housePricing)
* **Data Exploration and Analysis:** Conducted thorough data exploration by examining summary statistics, identifying missing values, and investigating the relationships between various features and the target variable (SalePrice).

* **Model Selection and Hyperparameter Tuning:** Employed a variety of regression models, including Linear Regression, Random Forest, and XGBoost, and performed hyperparameter tuning to optimize model performance. The best models were identified based on the root mean square error (RMSE).

* **Feature Engineering:** Engineered new features, such as property age, total living area, and total bathrooms, to improve model accuracy and capture valuable insights into housing prices. Categorical variables were appropriately encoded for modeling.

* **Principal Component Analysis (PCA):** Applied PCA for dimensionality reduction to reduce multicollinearity and enhance the efficiency of regression models while maintaining predictive performance.

* **Ensemble Modeling:** Employed ensemble techniques by combining predictions from different models (Random Forest, XGBoost, and a Multilayer Perceptron Regressor) to create a more robust and accurate final prediction.
![](/images/1.png)
![](/images/2.png)
![](/images/3.png)


<br>
<br>
