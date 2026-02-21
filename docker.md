# What is Docker?

Docker is an open-source platform that uses **containerization** to package an application and all its dependencies (libraries, configuration files, etc.) into a single unit called a **container**. 

Docker creates an environment where all the required libraries are pre-installed within that container, ensuring the application runs the same way everywhere.

Problem it Solves: The classic "Works on my machine" problem. It ensures that if an app runs on a developer's Windows laptop, it will run exactly the same on a client's Mac or a Linux server

Docker is an open-source platform that uses containerization to package an application and all its dependencies into a single unit called a container. and then we ship this container to the client via image and we can run this image on any computer

in docker we are creating virtual env or creating container and because of that virtual env it works on different computer

Problem Solved: The "Works on my machine" syndrome.

Origin: Introduced in 2013 by DotCloud; now part of the CNCF.

Core Value: Provides a consistent environment from development to production.

### Key Components:
* **The Image:** A read-only template (the blueprint).
* **The Container:** A running instance of that image (the actual house).
* **The Docker Engine:** The software that runs the containers.

---

# Why do we use it?

The main reason is **consistency**. It solves the classic *"It worked on my machine!"* excuse by ensuring the environment is identical across development and production.

| Benefit | Description |
| :--- | :--- |
| **Portability** | Build it once, run it anywhere (Mac, Windows, Linux, or Cloud). |
| **Isolation** | Each container is separate. You can run one app using Python 2 and another using Python 3 on the same server without conflicts. |
| **Efficiency** | Unlike Virtual Machines (VMs), containers share the host's OS kernel. They start in seconds and use very little RAM. |
| **Scalability** | You can spin up 10 identical copies of a web server instantly to handle a spike in traffic. |

---

# How it works (The Workflow)

1.  **Write a Dockerfile:** A simple text file with instructions on how to build your app.
2.  **Build an Image:** Docker turns that file into a portable, static image.
3.  **Run a Container:** You (or a server) run that image to start your application as a live process.

# Virtualization vs. Containerization

## Comparison Overview: Virtualization vs. Containerization

| Feature | Virtualization (VMs) | Containerization (Docker) |
| :--- | :--- | :--- |
| **Management Layer** | Uses a **Hypervisor** to manage multiple independent operating systems. | Uses a **Docker Engine** (or tools like Podman/Containerd) to manage containers. |
| **OS Structure** | Each Virtual Machine (VM) includes its own full **Guest OS**. | Containers do not have their own OS; they share the **Host OS kernel**. |
| **Resource Usage** | **Heavyweight**: Requires significant RAM and CPU to run a full OS. | **Lightweight**: Much smaller as they only package necessary libraries and code. |
| **Efficiency** | On an 8GB machine, you might only run 1 or 2 VMs. | On an 8GB machine, you can run dozens of containers simultaneously. |


Architecture Differences

Virtual Machines: Sit on top of a Hypervisor, which manages hardware resources for multiple Guest OS instances (Windows, Mac, or Linux).

Containers: Run on top of the Docker Engine and utilize the Host OS resources directly without needing a separate Guest OS layer.

docker pull - just pull the file

docker run - pull and run the file
we can create or pull inbuilt image,here we are pulling hello-world image and running
<img width="2940" height="1912" alt="image" src="https://github.com/user-attachments/assets/7acc446e-e2e1-43a8-a646-10ec29f6f2a7" />

to see all the command, use docker command

First, we create a Dockerfile, which serves as a 'Chitthe' or a list of instructions. We provide all the necessary commands in this file to build an Image. Once built, this image acts as a read-only blueprint containing the application code and all required libraries. Finally, we run this image to create a Container, which is the live, runnable instance of the application.

And we can pull a prebuilt Docker image

Dockerfile: The Instruction Set.

Image: The Blueprint .

Container: The Runtime Instance.
<img width="2940" height="1912" alt="image" src="https://github.com/user-attachments/assets/a4bd780c-1375-4283-9b40-3316255d3a1d" />
we can run the code in terminal or docker terminal
<img width="2940" height="1912" alt="image" src="https://github.com/user-attachments/assets/40121ec5-df37-4d46-b02f-b51cea67b6d4" />

we can pull image from docker hub 
<img width="2940" height="1912" alt="image" src="https://github.com/user-attachments/assets/ce5ac444-5aca-4e4a-94ee-07004e863d44" />
lets run busybox
<img width="2940" height="1912" alt="image" src="https://github.com/user-attachments/assets/691f262b-9cdd-465b-a07b-3cf788392e75" />
docker ps -a command wil show all running containers id and all
<img width="2940" height="1912" alt="image" src="https://github.com/user-attachments/assets/068a1490-18be-4e51-ab21-3a4b4fc5b46b" />

docker stop container_id -- to stop the container

docker images -- we can see all the image
<img width="2940" height="1912" alt="image" src="https://github.com/user-attachments/assets/c02c0251-c233-4819-bfc5-674fda0eb07d" />
<img width="2940" height="1912" alt="image" src="https://github.com/user-attachments/assets/c02c0251-c233-4819-bfc5-674fda0eb07d" />

docker run -d busybox -- it will run the container in the background keep my terminal free

to get all the command just run--  docker

to remove any docker -- docker rm id

<img width="2940" height="1912" alt="image" src="https://github.com/user-attachments/assets/a57a3d62-6b8d-4cd3-9557-31ea1214671f" />




