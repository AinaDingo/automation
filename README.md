# Automation
## NGINX
First, install NGINX and run the init-letsencrypt.sh (only once) to get certificate generated.
This certificate will be used by gitlab

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