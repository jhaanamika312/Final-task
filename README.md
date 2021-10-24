# Final-tasks
# **SENTIMENT MODEL**

## Use of the webpage
It takes sentence as the input from user and predict the sentiment as the output. To determine sentiment following libraries are used:
Flask
Sklearn
Vader Sentiment
NLTK
Requests
re
### VADER Sentiment
VADER (Valence Aware Dictionary and sEntiment Reasoner) is a lexicon and rule-based sentiment analysis tool that is specifically attuned to sentiments expressed in social media, and works well on texts from other domains.

## File of the repo
The app.py file is a flask webserver that host the sentiment analysis model and act as producer of rabbitmq
The worker.py file is the rabbitmq worker that recives the message from the producer 
The requirement.txt file has the necessary libraries and requirements need to run the code
The dockercompose.yml file is to build docker image and run the container

## How to run it
1.Install the dependencies from requirement.txt 

2.In server folder run app.py and from worker folder run worker.py

Note:- I am facing an error that after running app.py the sentiment model run on webserver but the worker.py file doesn't get connected to it and it doesn't shows any output recieved and thus the message in worker queue remains empty.

3.To run the docker image run 'docker-compose up -d' three image for server ,rabbitmq image and worker gets started.

Note: When i am creating an network in docker compose file it gives me error "service.networks must be mapping" but without specifying an network in the compose file the docker conatiner runs well

## Output
Output of the code in mp4 format is included in the folder 'output'
