# Introduction to Docker

A beginner-friendly introduction to Docker, covering its purpose, architecture, and installation on an AWS EC2 instance.

## 🎯 What is Docker?

Docker is a containerization platform that allows applications and their dependencies to be packaged together into lightweight, portable containers.

Containers can run consistently across different environments, making application deployment easier and more reliable.

---

## 🆚 Docker vs Virtual Machines

### Virtual Machines (VMs)

* Each VM includes a complete Guest Operating System.
* Requires more CPU, memory, and storage resources.
* Slower startup time due to the overhead of running multiple OS instances.

### Docker Containers

* Share the Host Operating System kernel.
* Lightweight and resource-efficient.
* Start much faster than Virtual Machines.
* Ideal for modern application deployment and microservices.

---

## 🏗️ Docker Architecture

Docker consists of several components working together:

### Docker Engine

The core runtime responsible for building and running containers.

### Docker Daemon (`dockerd`)

A background service that manages Docker objects such as:

* Containers
* Images
* Networks
* Volumes

### Docker CLI

The command-line interface used to interact with Docker.

Example:

```bash
docker ps
docker images
docker run nginx
```

### Docker Client

The client communicates with the Docker Daemon using Docker APIs and executes user commands.

---

## ⚙️ Hands-On Practice

### AWS EC2 Setup

Created an Ubuntu EC2 instance and connected via SSH.

### Update Package Repository

```bash
sudo apt-get update
```

Updates the Ubuntu package index with the latest available packages.

### Install Docker

```bash
sudo apt-get install docker.io -y
```

Installs Docker on the Ubuntu instance.

### Verify Docker Service

```bash
sudo systemctl status docker
```

Checks whether the Docker service is running.

### Add Current User to Docker Group

```bash
sudo usermod -aG docker $USER
```

Allows running Docker commands without using `sudo`.

### Apply Group Changes

```bash
newgrp docker
```

Refreshes group membership without logging out.

### Verify Docker Installation

```bash
docker ps
```

Displays running containers and confirms Docker is working correctly.

---

## 📚 Key Learnings

* Docker is a containerization platform that packages applications with their dependencies.
* Containers are lightweight compared to Virtual Machines.
* Docker uses the host operating system's kernel, reducing resource consumption.
* Docker Engine, Daemon, CLI, and Client are the core architectural components.
* Docker can be easily installed and managed on an AWS EC2 instance.

---

## 🛠️ Commands Used

```bash
sudo apt-get update
sudo apt-get install docker.io -y
sudo systemctl status docker
sudo usermod -aG docker $USER
newgrp docker
docker ps
```