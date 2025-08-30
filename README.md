<<<<<<< HEAD
# ta_mars_docker
=======
# MVP Studio - Project Mars

### 1. Install Docker
Ensure you have the latest version of Docker installed. You can download it from Docker's official website. Follow the instructions for your operating system.

### 2. Running Docker
1. After downloading the Docker files, open CMD or PowerShell/Terminal.
2. Navigate to the root directory of the downloaded files using: `cd {path-to-directory}` eg: `cd /Users/{yourname}/Downloads`
3. Then, to start the server and services, run: `docker compose up`
4. To stop and remove running containers, use: `docker compose down`

### 3. Important Notes
* **Windows Users**: Ensure Docker is set to run in Linux Containers mode before executing the commands (Right click bottom right Docker Icon and you should be able to see the option to switch).
* **Project URL**: http://localhost:5003
* Make sure Docker is updated to the latest version to avoid compatibility issues.

### Resources
* You need to download this file for running the docker: `docker-compose.yml`
* More Tutorial: https://www.youtube.com/watch?v=HG6yIjZapSA

---

## MongoDB Setup for Mars Project

### For new users:
1. Just run:
   ```
   docker-compose up
   ```

### Existing user who download Mars before and have missing data(eg, category):
1. Stop all existing docker services if any:
   ```
   docker-compose down
   ```

2. Run the service again:
   ```
   docker-compose up -d mongodb
   ```

3. Run the following script to populate data:
   ```
   docker-compose run mongodb-seeder
   ```
>>>>>>> 932962e (Initial commit)
