# Docker Cheat Sheet

### Searching for docker images:

```bash
docker search redis
```

### Run docker images:

```bash
docker run -d redis
```
-d detached command (run in background)

---
**NOTE**

By default, Docker will run the latest version available. If a particular version was required, it could be specified as a tag, for example, version 3.2 would be: __docker run -d redis:3.2__

---


### Check running docker containers:

```bash
docker ps
```

### Provide more informaiton about particular instance:

```bash
docker inspect <id>
```

### Check logs from particular instance:

```bash
docker logs <id>
```

### Use "fancy name" during creating instance:

```bash
docker run -d --name <fancy name> redis
```

---
**NOTE**

Fancy name can be used with **inspect** and **logs**

---

### Redirect ports from inside docker container to outside:

```bash
docker run -d --name RedisFancyName -p <hostPort>:<containerPort> redis:latest
```

---
**NOTE**

By default, the port on the host is mapped to 0.0.0.0, which means all IP addresses. You can specify a particular IP address when you define the port mapping, for example: __-p 127.0.0.1:6379:6379__

---
 
 
### Binding directories (volumes) from host to container:

```bash
docker run -d --name RedisMapped -v <host dir>:<container dir> redis:latest
```

---
**NOTE**

Docker allows you to use $PWD as a placeholder for the current directory.

---

### Run command inside container:

```bash
docker run -it redis ps
```

---
**NOTE**

If it is needed to get inside container with /bin/bash command line, the command at the end of the one-liner should be __bash__

---