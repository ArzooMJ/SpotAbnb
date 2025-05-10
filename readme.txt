### REQUIRED FILES: ###
ensure you have a file called .env that contains the following API keys:
DISCOVERY_KEY = REDACTED
GMAPS_KEY = REDACTED
SPOTIFY_KEY = REDACTED
########################

HOW TO RUN:

Open main.py and run the file. 

IMPORTANT: on line 19, the function call to spotify's api is commented out. 
The way Spotify manages their tokens is that they expire every hour due to security. 
As a work around, I've left my spotify_data.json file within.
Simply running main.py as is will take the data extracted from this file for the rest of the file (which should be fine). 

HOWEVER, should you want to run it with your own spotify account login, then please email me. (jiwani.a@northeastern.edu) 
Spotify's API requires me to approve users with a token that expires. I will try to add you before you test it, but I need your email associated with your spotify account to do so. 

Once added, AND uncommented line 19, delete .cache if it is there. 
Running again should force you to log in to spotify. 
##############################
Overview

1. Authenticates and fetches user data from Spotify.

2. Recommends nearby concerts using the Ticketmaster API.

3. Finds Airbnbs near the concerts.

4. Scores Airbnbs based on distance, price, and Google Maps routing data.

5. Ranks recommendations using XGBoost and Deep Neural Networks.

6. Opens a browser-based report with top suggestions.
###############################
Technologies & APIs Used

Spotify API – To get user’s top artists and genres.

Ticketmaster API – To find concert events based on Spotify data.

Google Maps API – For distance and travel time calculations.

XGBoost – For machine learning-based Airbnb recommendations.

Keras/TensorFlow (DNN) – For deep learning recommendations.

Pandas – For data manipulation.

dotenv – To manage API keys securely.

#####################################
