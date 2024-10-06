Portainer is a container management tool, but I still prefer using Docker Compose for deploying containers whenever possible. I mainly use Portainer to get an overview of all my Docker containers in one dashboard and to perform simple tasks like checking status, viewing logs, or restarting containers.

<https://docs.portainer.io/start/install-ce/server/docker/linux>

For installations that don’t provide a Docker Compose file, tools like Composerize can help. It converts the provided docker run commands into Docker Compose format for easier management.

``` py title="docker-compose.yaml"
services:
    portainer-ce:
        container_name: portainer
        image: portainer/portainer-ce:latest
        ports:
            - 8000:8000
            - 9443:9443
        volumes:
            - /var/run/docker.sock:/var/run/docker.sock
            - /opt/portainer/data:/data # please change /opt/portainer/data to your own directory
        restart: always
```