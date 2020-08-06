#MakeViral
This application can predict the popularity tweets, improve the text in the tweets ro gain  more popularity and finally predict the enhanced popularity.

Clone the repository to your local environment. 

Create a virtual environment. And install the required dependencies with "pip3 install requirements.txt"

Run app.py

a) You can get the intial prediction with the following request. 

curl --location --request POST 'http://127.0.0.1:5000/predict_initial' \
--header 'Content-Type: application/json' \
--data-raw '{
    "tweet": {
        "text": "This lipstick is so good and beautiful"
    }
}'

b) You can get the enhanced prediction with the following request. 

curl --location --request POST 'http://127.0.0.1:5000/improve_tweet' \
--header 'Content-Type: application/json' \
--data-raw '{
    "tweet": {
        "text": "This lipstick is so good and beautiful"
    },
    "initial_reach": 3166,
    "initial_retweet_count": 158,
    "initial_favourite_count": 219
}'
