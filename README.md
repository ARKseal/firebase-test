# firebase-test
This is a test for firebase hosting

## Setup:
1. make a virutal enviroment (venv) and activate it
    * Windows: `python -m venv venv` and activate using `.\venv\Scripts\activate`
    * Linux/Mac: `python3 -m venv venv` and activate using `source ./venv/bin/activate`
    * deactivate using `deactivate`
2. install dependencies by running `pip install -r requirements.txt`
3. run app using `python app.py`

## Run on Docker:
1. cd into server `cd ./server`
2. build docker image using `docker build -t crescendoforacause-server .`
3. run docker image using `docker run -dp 8080:8080 crescendoforacause-server`
4. see output with url: `http://localhost:8080/`

## Firebase Node hosting
1. run `npm init -y` to initialize node
2. install using `npm install -D firebase-tools`
3. run `./node_modules/.bin/firebase init hosting` to initialize hosting
4. remove static index.html
    * Windows: del static\index.html
    * Linux/Mac: rm static/index.html
5. Run using `./node_modules/.bin/firebase serve`

## To Deploy:
1. send new build using `gcloud builds submit --tag gcr.io/<project-id>/flask-fire`
2. run using `gcloud beta run deploy --image gcr.io/<project-id>/flask-fire`
2. deploy using `firebase deploy`