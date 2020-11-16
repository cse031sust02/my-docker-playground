# FROM - Image to start building on.
FROM python:3

# sets the working directory
WORKDIR /usr/src/myapp

# install pipenv
RUN pip install pipenv

# copy our Pipfile and Pipfile.lock to container
COPY Pipfile ./
COPY Pipfile.lock ./

# install all required packages
RUN set -ex && pipenv install --deploy --system

# copy all files from host to container
COPY . .

# set environment
ENV FLASK_APP=hello.py

# expose the port
EXPOSE 5000

# Command to run
CMD ["flask", "run", "--host=0.0.0.0"]
