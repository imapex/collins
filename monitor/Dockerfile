FROM ubuntu
WORKDIR /code
ADD ./requirements.txt /code
RUN apt-get update && apt-get install -y python-pip
RUN pip install -r requirements.txt
ADD . /code
CMD  celery -A api.tasks ----broker=$RABBITMQ_URL flower
