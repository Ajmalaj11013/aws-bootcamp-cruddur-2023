FROM python:3.10-slim-buster

# inside the conatiner
WORKDIR /backend-flask

# outside container -> inside container
COPY requirements.txt requirements.txt

# inside container
# install the python libraries used for the app/
RUN pip3 install -r requirements.txt

# copy contents from outside container -> inside container
# . means conents in the current directory
# first period represnt /backend-flask(outside container)
# second flask represent /backend-flask inside the container. 
COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]