# Linux Web Server

A simple web server project built with **Nginx**, **Docker**, and **Docker Compose**.

This project serves a static website through an Nginx container and demonstrates basic Linux web hosting concepts.

---

## Overview

The website is hosted inside a Docker container running Nginx. The web content is mounted into the container and served on port 8082.

This project was created as part of a Linux home lab to practice:

* Docker
* Docker Compose
* Nginx
* Linux server administration
* Web hosting fundamentals

---

## Architecture

```text
Browser
   │
   ▼
localhost:8082
   │
   ▼
Docker Container
   │
   ▼
Nginx
   │
   ▼
Static Website
```

---

## Technologies Used

* Linux / WSL2
* Docker
* Docker Compose
* Nginx
* Git
* GitHub

---

## Features

* Containerized Nginx web server
* Custom HTML website
* Docker Compose deployment
* Custom Nginx configuration
* Static content hosting

---
## Screenshots
Homepage
<img width="1918" height="875" alt="Schermafbeelding 2026-06-22 120602" src="https://github.com/user-attachments/assets/3c681952-75e6-478c-9528-9cf35b0024bc" />

About Page
<img width="1919" height="873" alt="Schermafbeelding 2026-06-22 120521" src="https://github.com/user-attachments/assets/021a7d3e-6826-4d05-88a5-6436f816975f" />

Health Endpoint

<img width="366" height="67" alt="Schermafbeelding 2026-06-22 120618" src="https://github.com/user-attachments/assets/ca3a9bf1-e1bf-4b6c-96c8-9f234e728c43" />

## Project Structure

```text
linux-web-server/
├── docker-compose.yml
├── nginx/
│   └── default.conf
├── site/
│   ├── index.html
│   └── about.html
└── README.md
```

---

## Running the Project

Start the web server:

```bash
docker compose up -d
```

Verify the container is running:

```bash
docker compose ps
```

Open the website:

```text
http://localhost:8082
```

---

## Nginx Configuration

The Nginx container uses a custom configuration file:

```nginx
server {
    listen 80;
    server_name localhost;

    root /usr/share/nginx/html;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}
```

---

## Screenshots

### Homepage

*Add screenshot here*

### Docker Container

*Add screenshot here*

### Nginx Configuration

*Add screenshot here*

---

## What I Learned

* Running web servers inside Docker containers
* Using Docker Compose to manage services
* Creating and serving static websites with Nginx
* Managing Linux-based web infrastructure
* Version controlling infrastructure projects with Git and GitHub

---

## Future Improvements

* HTTPS with SSL certificates
* Nginx reverse proxy configuration
* Custom domain name
* Multiple hosted websites
* Integration with monitoring stack (Prometheus + Grafana)

---

## Status

Project completed and running successfully using Docker Compose and Nginx.
