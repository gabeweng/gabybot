# gabybot
This is a simple chatbot. It will respond to your questions and statements.
## How to run
Run the following command to launch a docker image
```
docker run -d -p 5005:5005 -p 5002:5002 -p 80:80 -p 8888:8888 --name rasa -e GRANT_SUDO=yes --user root -e JUPYTER_ENABLE_LAB=yes -v %cd%:/home/jovyan cliffweng/cory
```
After the docker container is up and running, run these in the container prompt
```
git clone https://github.com/gabeweng/gabybot.git
cd gabybot
rasa train
rasa run actions &
rasa x
```
