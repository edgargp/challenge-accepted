FROM python:3.9-slim-buster
RUN mkdir /app
ADD . /app
WORKDIR /app
ENV HTTP_PORT=5000 \
    JWT_SECRET=secret
RUN pip3 install -r requirements.txt
CMD [ "python3", "main.py"]
HEALTHCHECK CMD curl --fail http://localhost:5000/health || exit 1