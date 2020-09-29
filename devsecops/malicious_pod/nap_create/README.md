## Prepare the 'NGINX App Protect' container image

### Configuration Step
#### *Please make sure that you already have the evaluation license from the F5 for your NAP.* 
#### *The evaluation license includes 1x'.crt' file and 1x'.key' file. These are required in this step.*
### *You need to have your own 'Docker Hub' account.*

### Create Dockerfile to build the 'NGINX App Protect' base image
You can find more detailed explanation from the document portal of the NGINX [here](https://docs.nginx.com/nginx-app-protect/admin-guide/#docker-deployment).
Below is the sameple 'Dockerfile' config which used in this demo. 

```
Dockerfile

# For CentOS 7:
FROM centos:7.4.1708

# Download certificate and key from the customer portal (https://cs.nginx.com)
# and copy to the build context:
COPY nginx-repo.crt nginx-repo.key /etc/ssl/nginx/

# Install prerequisite packages:
RUN yum -y install wget ca-certificates epel-release

# Add NGINX Plus repo to Yum:
RUN wget -P /etc/yum.repos.d https://cs.nginx.com/static/files/nginx-plus-7.repo
    
# Install NGINX App Protect:
RUN yum -y install app-protect \
    && yum clean all \
    && rm -rf /var/cache/yum \
    && rm -rf /etc/ssl/nginx
 
# Forward request logs to Docker log collector:
RUN ln -sf /dev/stdout /var/log/nginx/access.log \
    && ln -sf /dev/stderr /var/log/nginx/error.log
        
# Copy configuration files:
COPY nginx.conf custom_log_format.json /etc/nginx/
COPY entrypoint.sh  ./
    
CMD ["sh", "/entrypoint.sh"] 
```

And build your docker image for NAP. (You have to place your NGINX 'crt' and 'key' files on the same directory.)
```
sudo docker build --no-cache -t app-protect .
```




