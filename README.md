# Jenkins docker
* Jenkins CI with docker client

#####Commands:
 - `docker build -t jenkins-docker-image .`
 - `docker run -p 8080:8080 -p 50000:50000 -v /var/jenkins_home:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock --name jenkins-container -d jenkins-docker-image`