ML zoomcamp Midterm Project

Dataset - cars.csv

Objective - to predict the used cars price in India.

Data Dictionary
●Id: Unique ID assigned to a specific car

●year: Manufacture year of the car

●brand: Brand of the car

●full_model_name: Model name includes other details such as engine capacity, transmission,etc., basically a detailed model name

●model_name: Just the model name of the car

●price: Sell price of the 2nd ownership car. (Note - prices are in INR - Indian Rupee)

●distance_travelled(km): Distance traveled by car

●fuel_type : Fuel engine type

●city: City where the car is registered

●car_age: Age of the car

we will do extensive EDA to obtain most important features, derive new features and train and tune couple of different ML models and select best model
to finally train the model and use test data to predict the test data.

all the extensive analysis is done in the notebook - mid-term-project-2026.ipynb

Highlights
1) check duplicate data if any and drop
2) check any redundant features (features telling same thing, for ex- car_age and year of manufacture)
3) check most important features that tells more about our target, which is price
4) tune randomforest model and tune for most important parameters
5) tune xgboost model and tune for most important parameters
6) finally conclude the model and parameters we use for train and finally train the model with the same
7) test with some test data

HOW to RUN

step 1
------
pull the docker hub image from docker

docker pull rkarji/car-price-prediction:latest

step 2
------
run the container

docker run -d -p 9696:9696 --name car-price-service rkarji/car-price-prediction:latest

step 3
------
Download the test script and run the test script.

file path - https://github.com/rkarji123/mlzoomcamp_rama/blob/main/mid-term-project/car_price_predict_test.py

python car_price_predict_test.py

step 4
------
stop and remove the container

docker stop car-price-service
docker rm car-price-service
