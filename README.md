# Docker Tutorial for IFT 6758 Lab
![image](https://user-images.githubusercontent.com/20723780/143995444-96c1dcc1-8124-4989-b427-43299eb4ca43.png)


In this repository, we examine advtanges of virtualization, what Docker is and how we can deploy simple programs on Docker.

Firstly, we will start by listing some advantages of virtualization. We can give discuss them as follows: 

- Minimize hardware costs (Multiple virtual servers on one hardware unit).
- Easily for HA (High Availability) And Disaster Recovery (DR). 
- Easier to save money and save energy, could be potentially _greener_. 

Problems with Virtualization: 

- Hard to maintain each OS, installation, HyperVisor and host OS compatibility issues, and HyperVisor - container issues. 
- Costly and might take IT/Programming effort.
- We might need a high storage overhead, even lightweight OSs with all tools installed can bulk up to a high size.

![image](https://user-images.githubusercontent.com/20723780/143990359-17532e37-62fc-4fc0-8e23-c7914ff1b430.png)

### Solution? 

- Use containers! 

### Container definition: 

- is a runnable instance of an image. 
- can be run on local machines, virtual machines or deployed to the cloud.
- is portable (can be run on any OS).
- Containers are isolated from each other and run their own software, binaries, and configurations.

### Methodology: 
- These applications share a parent application and its overhead. 
- These apps can run separately, and we can avoid multithreading issues, deadlock issues and other issues with RPCs that may arise. 
- They can't access each other's resources, and they are like apartments in a complex. 

### Container Architecture: 

![image](https://user-images.githubusercontent.com/20723780/143990532-bc3b9d6b-1d67-4753-8b18-6f6cd4d2186f.png)

- Multiple containers run on the same machine virtual / physical machine. 
- All containers share the same OS and Kernel. 
- We can micro-manage processes, and have a higher level and more fine-grained access. 
- We can stop processes using the power of the host OS, and we can even save/move states as we need. 
- We can run containers inside VM! It's interesting as we can combine the power of both if we have a very specialized applicaiton. 
- Higher security as we are working with a very simple isolated block of code.


### Compute Comparision:

![image](https://user-images.githubusercontent.com/20723780/143990826-2309c269-5e52-48b3-ac73-fa58de183542.png)

### Docker: 

- Does exactly what we need, and it assists in efficient containerization. 
- Free and Open Source! (now under Moby)
- Helps in packaing source code, libraries, dependencies, volumes, routes, etc for production.
- The name Docker had roots from the word "Dock Worker", assists in effective container management. 
- Containers are built from _images_ and saved as _images_. 
- Each image is identified by a UUID/256 Bit Hash. 
- Each Docker Image has several tags, and we can help in effective versioning. 
- Dockers can be secured by SSH, and additional network security techniques. 

![image](https://user-images.githubusercontent.com/20723780/143991344-12ac2ac0-7bbc-444d-b43d-aeb92ec1d430.png)

![image](https://user-images.githubusercontent.com/20723780/143991532-b8d7e0d5-070b-4d01-aa6c-1ce058a0967e.png)

### Dockerfile:

- Dictates the program installation, setup, packaging, instructions, port exposition, etc. 
- We can run a container, list a container, version them, delete them, etc. 

### Tools: 

- `Docker Compose`: It us used for maintaining and running multi-container Docker applications. We use YAML (mark-up) to dictate the format, dependencies and other nuances of a project. It can aid in building and scaling containers.
- `Docker Volume`: We can store and manage separate volumes of code, that avoid deletion when the container is stopped. 

## References:

1. https://runnable.com/docker/python/docker-compose-with-flask-apps
2. https://github.com/docker/awesome-compose
3. https://docs.docker.com/language/python/build-images/
4. https://www.cse.wustl.edu/~jain/cse570-18/ftp/m_21cdk.pdf
5. https://en.wikipedia.org/wiki/Docker_(software)
6. https://docs.docker.com/compose/
