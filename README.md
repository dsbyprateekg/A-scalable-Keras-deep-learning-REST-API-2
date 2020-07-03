# Create a deep learning REST API that wraps a Keras model in an efficient, scalable manner using Redis

In this project I am going to utilize Redis as a message broker/message queue. This involves:

- Running Redis on our machine
- Queuing up data (images) to our Redis store to be processed by our REST API
- Polling Redis for new batches of input images
- Classifying the images and returning the results to the client

## Functionality

- Our model will predict image

## Environment

- Windows 10, Python 3.6, keras, Redis, Flask


## Blog
- I have detailed the steps in my blog also
```html
http://dsbyprateekg.blogspot.com/2019/03/how-to-use-redis-in-windows-along-with.html
```

## Installing

- Create and Activate virtual env using below commands- 
```
pip install pipenv
pipenv install
pipenv shell
```

- Follow below steps for installing Redis if you are using Windows
```text
Download latest of Redis from Redis for Windows link
Download file be in zip format like Redis-x64-3.2.100.zip
Create a new folder and extract downloaded zip file there
Navigate to extracted folder and open it in a cmd as an Admin
Run the following command:redis-server.exe
A pop up will come and ask you to allow access, accept the default. It will start the Redis server
Leave this terminal open to keep the Redis data store running
In another terminal, you can validate Redis is up and running by following command: redis-cli.exe ping
In response you will get a PONG back from Redis, it means you’re ready to go
```

## Running examples
- Make sure Redis server is up and running
- Run `python run_keras_server.py` wait till server is running
- Run `python simple_request.py`
