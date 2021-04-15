# Docker Cheat Sheet

### Searching for docker images:

```bash
docker search redis
```

### Run docker images:

```bash
docker run -d redis
```
-d deamonize command (run in background)

---
**NOTE**

__By default, Docker will run the latest version available. If a particular version was required, it could be specified as a tag, for example, version 3.2 would be:__ docker run -d redis:3.2

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

__Fancy name can be used with__ **inspect** __and__ **logs**

---

### 
