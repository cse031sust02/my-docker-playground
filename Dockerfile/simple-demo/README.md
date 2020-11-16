## A very simple demo
This is a very simple demo to get started with Dockerfile


## How to Run 
Let's start with a very simple example by creating a Dockerfile to run an ubuntu container. 

- I've created the *Dockerfile* with the following instructions:

```dockerfile
# Get the base ubuntu 18.04 from Docker hub
FROM ubuntu:18.04

# Command to execute when we run the container
CMD echo "Hello World!"
```

- Let's build an image from that Dockerfile.
```bash
user@pc:/simple-demo$ ls
Dockerfile

user@pc:/simple-demo$ docker build .
Sending build context to Docker daemon  2.048kB
Step 1/2 : FROM ubuntu:18.04
 ---> 56def654ec22
Step 2/2 : CMD echo "Hello World!"
 ---> Running in a49ebaf5c0f1
Removing intermediate container a49ebaf5c0f1
 ---> 339710e878e8
Successfully built 339710e878e8
```
We can see that the Docker image was successfully built and the ID of the image is **339710e878e8**. 

- Now, Let's start and run a container from that image.
```bash
user@pc:/simple-demo$ docker run 339710e878e8
Hello World!
```

So now we have an Ubuntu container running inside our machine. We can also enter the container, install new packages, and run commands in the same way as we would do on any other Ubuntu machine.