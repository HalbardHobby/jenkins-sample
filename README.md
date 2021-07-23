# Jenkins Sample Project

## Dockerizing Jenkins

```
docker run --rm -d -p 8080:8080 -p 50000:50000 --group-add $(stat -c '%g' /var/run/docker.sock) -v /home/halbard/jenkins:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock -v $(which docker):/usr/bin/docker jenkins/jenkins
```