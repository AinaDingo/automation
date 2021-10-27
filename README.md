# Automation 

## NGINX
First, install NGINX and run the init-letsencrypt.sh (only once) to get certificate generated.
The generated certificate will be used by gitlab during his installation.

### Gitlab
Install Gitlab, the first time, change root password inside the container, create repository and so on
```
bash$ docker exec -it gitlab bash
root@gitlab gitlab-rake "gitlab:password:reset[root]"
```

#### Backup
```
gitlab-rake gitlab:backup:create
```
