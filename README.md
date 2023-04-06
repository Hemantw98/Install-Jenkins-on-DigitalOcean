# Install-Jenkins-on-DigitalOcean

### Technologies used:
Jenkins, Docker, DigitalOcean, Linux

### Project Description:
Create an Ubuntu server on DigitalOcean Set up and run Jenkins as Docker container Initialize Jenkins

### Below are the steps to create an Ubuntu server on DigitalOcean, set up and run Jenkins as a Docker container, and initialize Jenkins:

Step 1: Create a new Droplet (virtual machine) on DigitalOcean and choose "Ubuntu" as the operating system. You can choose the size of the Droplet based on your needs and budget.

Step 2: Once the Droplet is created, SSH into it using a terminal or SSH client. You can find the IP address of the Droplet in the DigitalOcean control panel.

Step 3: Install Docker on the Ubuntu server using the following commands:

    sudo apt-get update
  sudo apt-get install -y docker.io
  
Step 4: Run the Jenkins Docker conatiner using the following command:

  docker run -p 8080:8080 -p 50000:50000 -d -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts
  
This command will start the Jenkins container and map ports 8080 and 50000 to the host machine. It will also create a volume named "jenkins_home" to persist data across container restarts.
  
Step 5: Once the Jenkins container is running, open a web browser and go to http://<Droplet IP address>:8080. This will bring up the Jenkins setup wizard.

Step 6: Follow the setup wizard to initialize Jenkins. You will need to create an admin user, install plugins, and configure Jenkins.

That's it! You now have a Ubuntu server running Jenkins as a Docker container.
