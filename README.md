# hardware/rainloop

![](https://i.goopics.net/nI.png)

### What is this ?

Rainloop is a simple, modern & fast web-based client. More details on the [official website](http://www.rainloop.net/).

### Features

- Lightweight & secure image (no root process)
- Based on Alpine
- Latest Rainloop **Community Edition** (stable)
- Contacts (DB) : sqlite, or mysql (server not built-in)
- With Nginx and PHP7

### Build-time variables

- **GPG_FINGERPRINT** : fingerprint of signing key

### Ports

- **8888**

### Environment variables

| Variable | Description | Type | Default value |
| -------- | ----------- | ---- | ------------- |
| **UID** | rainloop user id | *optional* | 991
| **GID** | rainloop group id | *optional* | 991
| **UPLOAD_MAX_SIZE** | Attachment size limit | *optional* | 25M
| **MEMORY_LIMIT** | Maximum amount of memory used by php | *optional* | 128M

### Docker-compose.yml

```yml
# Full example :
# https://github.com/hardware/mailserver/blob/master/docker-compose.sample.yml

rainloop:
  image: hardware/rainloop
  container_name: rainloop
  volumes:
    - /mnt/docker/rainloop:/rainloop/data
  depends_on:
    - mailserver
```

#### How to setup

https://github.com/hardware/mailserver/wiki/Rainloop-initial-configuration
