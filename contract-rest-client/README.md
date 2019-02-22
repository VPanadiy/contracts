# Build project
1. Move to project folder
2. Build a Docker Image with Maven: `mvnw install dockerfile:build`
3. To start project run (from docker daemon): `docker-compose up` 
4. Open project in browser `http://127.0.0.1:8080`.
    * Get ip address from docker toolbox run: `docker-machine ip` 
