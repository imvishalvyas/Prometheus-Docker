# Prometheus-Docker
Dockerfile to deploy prometheus 

### Download the promethes for linux. 
```
https://github.com/prometheus/prometheus/releases/download/v2.7.1/prometheus-2.7.1.linux-amd64.tar.gz
```

untar setup.
```
tar -xzf prometheus-2.7.1.linux-amd64.tar.gz
```
Go to the directory. 
```
tar -xzf prometheus-2.7.1.linux-amd64.tar.gz 
```
```
cd prometheus-2.7.1.linux-amd64
```
Now you can costumize you promethus.yml file and add some target into it and save the file.

## Create docker file.
### Dockerfile
```
FROM prom/prometheus
ADD . /etc/prometheus/
```
save the file.

## Build the Dockerfile.
```
docker build -t prometheus:myversion .
```
## Now run the Docker image.
```
docker run prometheus:myversion
```
Now you can check from browser with port 9090.
```
http://localhost:9000
```


#imvishalvyas #linuxguru
