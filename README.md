# Jenkins docker
* Jenkins CI with docker client

#### Commands:
 - `docker build -t jenkins-docker-image .`
 - `docker run -p 8080:8080 -p 50000:50000 -v /var/jenkins_home:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock --name jenkins-container -d jenkins-docker-image`
 
 
 Incase of an error, while running `docker ps` inside the container:
 
```Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: permission denied```

Run:
`sudo chown 1000:1000 /var/run/docker.sock`
