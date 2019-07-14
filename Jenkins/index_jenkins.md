# jenkins


## docker 安装

```shell
docker run \
  --rm \
  -u root \
  -p 8080:8080 \
  -v jenkins-data:/var/jenkins_home \ 
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v /Users/frankie/DockerHome:/home \ 
  jenkinsci/blueocean
  
# 密码
# 6a4be1c9568e43feae6772ce3cc3b489

```
