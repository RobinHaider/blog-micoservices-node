
# Blog Microservices

A simple blog app for demonstrating Microservices with node js, running with docker and kubernetes. Using async communicaton with custom event-bus.


## Features

- User can add post (Post Service)
- User can add comment on post (Comment Service)
- User can see all the post and comments (Query Service)
- User can't have "orange" in their comment, if they do it will be flagged. (Moderation Service)


## Services

- Comments Service
- Post Service
- Event-bus
- Moderation Service
- Query Service


## Tech Stack

**Client:** React, Axios

**Server:** Node, Express

**Deployment:** Docker, Kubernetes, Skaffold

**Kubernetes:** Deployment, ClusterIp Service, Load balancer, Ingress-nginx, 


## Installation

Clone the repository. Install docker and enable kubernetes. Install Skaffold Cli.

Edit your host file (if windows "C:\Windows\System32\drivers\etc\hosts"). Add this

```bash
  127.0.0.1 posts.com
```

Then inside blog-micoservices-node/infra/ingress-nginx/ run

```bash
  kubectl apply -f ingress-controller.yaml
```
Then in root folder run

```bash
  skaffold dev
```

Now visit

```bash
  posts.com:81
```
    
## Screenshots

![App Screenshot](https://github.com/RobinHaider/blog-micoservices-node/blob/main/Blog-Node-Microservice.png)

