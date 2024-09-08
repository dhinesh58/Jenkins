# Jenkins
Azure Infra creation using Terraform Jenkins Pipeline

Install the Jenkins

Installation of Java

Jenkins requires Java to run, yet not all Linux distributions include Java by default. Additionally, not all Java versions are compatible with Jenkins.

sudo apt update
sudo apt install fontconfig openjdk-17-jre

Installation of Java

sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt-get update
sudo apt-get install jenkins

Start Jenkins
Enable the Jenkins service to start at boot with the command:
sudo systemctl enable jenkins

Start the Jenkins service with the command:
sudo systemctl start jenkins

You can check the status of the Jenkins service using the command:
sudo systemctl status jenkins

If Machine have a firewall installed, you must add Jenkins as an exception. You must change YOURPORT in the script below to the port you want to use. Port 8080 is the most common.
