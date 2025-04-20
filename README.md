# docker-swarm-app

## Deploying to Docker Swarm (3 EC2 servers)

# On your manager node, initialize:
docker swarm init --advertise-addr <MANAGER-IP>

# Join the other 2 nodes:
docker swarm join --token <TOKEN> <MANAGER-IP>:2377

# Then deploy the stack:
docker stack deploy -c docker-compose.yml minhaapp

# Open the app via:
http://<nginx-ip>:4500

# Records will be inserted into MySQL from each replica.

