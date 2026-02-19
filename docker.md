## What is Docker?
Docker is an open-source platform that uses containerization to package an application and all its dependencies (libraries, configuration files, etc.) into a single unit called a container.
## The Image: A read-only template (the blueprint).
## The Container: A running instance of that image (the actual house).
## The Docker Engine: The software that runs the containers.

## Why do we use it?
The main reason is consistency. It solves the classic "It worked on my machine!" excuse.
BenefitDescriptionPortability - Build it once, run it anywhere (Mac, Windows, Linux, or Cloud).
IsolationEach container is separate. You can run one app using Python 2 and another using Python 3 on the same server without them fighting.
EfficiencyUnlike Virtual Machines (VMs), containers share the host's OS kernel. They start in seconds and use very little RAM.ScalabilityYou can spin up 10 identical copies of a web server instantly to handle a spike in traffic.
## How it works (The Workflow)
## Write a Dockerfile: A simple text file with instructions on how to build your app.

## Build an Image: Docker turns that file into a portable image.

## Run a Container: You (or a server) run that image to start your application.
