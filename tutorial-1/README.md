# README to understand this file: 

## Testing Flask in the vanilla way: 

```
python3 -m flask run
```

Then, if you navigate to your localhost and enter the site correctly, you will be able to see the server logs: 

```
127.0.0.1 - - [22/Sep/2020 11:07:41] "GET / HTTP/1.1" 200 -
```

As we know from basic HTML principles, an HTTP 200 means an `OK`. 

The directory structure for this folder is given as follows:

```
tutorial-1
|____ app.py
|____ requirements.txt
|____ Dockerfile
```

## Building an image:

```
 docker build --tag tutorial-1 .
```

## View local images:

```
docker images
```

## Tag / Version Images: 

```
docker tag tutorial-1:latest tutorial-1:v1.0.0
```

## Removing a tag:

```
docker rmi python-docker:v1.0.0
```

## Run image as a container:

```
docker run --publish 5000:5000 tutorial-1
```

## Testing the container in a terminal:

### UNIX:

```
curl localhost:5000
```

### Windows (Version >= 10):

```
curl.exe localhost:5000
```

If there is a success, you should see the following message: 

```
[31/Jan/2021 23:39:31] "GET / HTTP/1.1" 200 -
```

## Running in a detached mode: 

```
docker run -d -p 5000:5000 tutorial-1
```

## Listing containers: 

```
docker ps
```


