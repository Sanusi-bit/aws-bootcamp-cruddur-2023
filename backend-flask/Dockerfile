FROM python:3.10-slim-buster

#Creating a work directory in the container
WORKDIR /backend-flask

#Copy from the Docker Client to the container
COPY requirements.txt requirements.txt

#Run the file inside the container to install the python libraries
RUN pip3 install -r requirements.txt

# . means Period. Copying from the working directory on the client to the container
COPY . .

#Setting the environment variables inside the container
ENV FLASK_ENV=development

EXPOSE ${PORT}

#Command to run the flask framework for python for the container
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]