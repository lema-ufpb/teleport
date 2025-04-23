## Teleport Deployment using Docker

This document outlines how to deploy Teleport, a modern security platform for accessing servers, applications, and databases, using Docker. Docker provides a consistent and isolated environment, simplifying the deployment and management of Teleport.

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- **Docker Engine:** Version 20.10 or later is recommended. Follow the official Docker installation guide for your operating system: [https://docs.docker.com/engine/install/](https://docs.docker.com/engine/install/)
- **Docker Compose:** Version 1.29 or later is recommended. Docker Compose is usually installed along with Docker Desktop. If you installed Docker Engine separately, you might need to install Docker Compose separately: [https://docs.docker.com/compose/install/](https://docs.docker.com/compose/install/)

## Add admin user

```bash
docker exec -it teleport tctl users add <username> --roles=editor,access --logins=root,<username>
```
