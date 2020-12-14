# Run Stacks 2.0 Testnet Mining Node using Docker
Read more at https://daemon-technologies.github.io/docs/

## Getting started

1) Install Docker and Docker compose

   ```
   https://docs.docker.com/engine/install/#server
   https://docs.docker.com/compose/install/
   ```
   
2) Clone Repo
   
   ```
   git clone https://github.com/viraja1/stacks-mining-docker.git
   cd stacks-mining-docker
   ```
   
3) Build Image

   ```
   docker-compose -f docker-compose.yml build
   ```
   
4) Run the containers in background

   ```
   docker-compose -f docker-compose.yml up -d
   ```   
   
5) Check logs of the mining server container

   ```
   docker logs -f stacks-mining-docker_mining_server_1
   ```
   
6) Check logs of the mining bot container

   ```
   docker logs -f stacks-mining-docker_mining_bot_1
   ```
   
7) Generate bitcoin and stacks wallet details

   ```
   docker run -i node:14-alpine npx @stacks/cli make_keychain -t 2>/dev/null
   ```
   
   Note down the details securely
   
8) Check the Mining bot dashboard once it is up
   ```
   http://localhost:8000/
   ```
   
   Then follow the following documentation to setup the Mining bot dashboard
   ```
   https://daemon-technologies.github.io/docs/Mining-Bot-Alpha-Version/Use-Mining-Bot-For-Mining/User's-Guide-of-Mining-Bot.html
   ```
