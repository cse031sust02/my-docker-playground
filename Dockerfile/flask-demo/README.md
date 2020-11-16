## Demo Flask Application
This is a simple demo for running a Flask application using Pipenv and Dockerfile


## Running using Docker

- Build the Docker image
```
docker build . --tag simple-flask-app
```

- Run the Docker container
```
sudo docker run -p 5000:5000 --name flask-container simple-flask-app
```

The app should be available now at [http://localhost:5000](http://localhost:5000/)