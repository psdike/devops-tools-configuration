# Jenkins and Docker Installation

This script installs Jenkins and Docker on a Debian-based system and configures them to work together. It also installs OpenJDK 11, which is required for Jenkins to run.

## CommandsThe following commands are executed in the script:


1. `curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null`: 

   This command downloads the Jenkins repository key and saves it to `/usr/share/keyrings/jenkins-keyring.asc`.

2. `echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > //null`: 

   This command adds the Jenkins repository to the system's list of package sources.

3. `sudo apt-get update -y`: 

   This command updates the package list on the system.

4. `sudo apt install openjdk-11-jdk -y`: 

   This command installs OpenJDK 11, which is required for Jenkins to run.

5. `sudo apt-get install jenkins -y`: 

   This command installs Jenkins on the system.

6. `sudo apt-get install docker.io -y`: 

   This command installs Docker on the system.

7. `sudo usermod -aG docker jenkins`: 

   This command adds the `jenkins` user to the `docker` group, which allows Jenkins to interact with Docker.

8. `sudo service jenkins restart`: 

   This command restarts the Jenkins service to apply the changes made in the script.
