# Known Sensitive Paths

This document tracks sensitive files, directories, and endpoints commonly targeted by Internet-wide vulnerability scanners.

Only paths with practical security value should be included in the Enterprise Path Block rule.

---

# Environment Files

```
.env
.env.local
.env.production
.env.development
.env.test
```

---

# Source Control

```
.git/
.git/config
.git/HEAD
.git/index

.svn/

.hg/
```

---

# Cloud Credentials

```
.aws/

.aws/credentials

.azure/

.gcp/

credentials.json
```

---

# SSH

```
.ssh/

authorized_keys

id_rsa

known_hosts
```

---

# Docker

```
Dockerfile

docker-compose.yml

docker-compose.yaml

docker.sock

.devcontainer/
```

---

# Kubernetes

```
kubeconfig

.kube/

helm

skaffold.yaml

tiltfile
```

---

# Terraform

```
terraform.tfstate

*.tfvars
```

---

# CI/CD

```
.github/

.gitlab/

.circleci/

.travis.yml

Jenkinsfile

buildspec.yml

pipelines.yml
```

---

# AI IDE

```
.cursor/

.cursorignore

.codeium/

.claude/

.continue/

.roo/

.mcp/

mcp.json

openhands/

windsurf/
```

---

# PHP

```
phpinfo.php

phpunit

composer.json

composer.lock
```

---

# WordPress

```
wp-login.php

wp-config.php

xmlrpc.php

wlwmanifest.xml
```

---

# Laravel

```
_ignition/

storage/logs/

laravel.log

debug.log
```

---

# Spring Boot

```
actuator

heapdump

beans

metrics

env
```

---

# Database

```
dump.sql

database.sql

backup.sql

backup.zip

.sql
```

---

# Logs

```
debug.log

error.log

access.log

laravel.log
```

---

# Secrets

```
.htpasswd

config.yml

config.yaml

config.php

secrets.yml
```

---

# API

```
swagger

swagger-ui

api-docs

openapi.json
```

---

# Future Candidates

These paths are under observation and may be added in future releases after sufficient evidence:

- Claude Code
- Gemini CLI
- Cursor Agent
- Roo Code
- OpenHands
- MCP Server
- Dev Containers
- OCI
- Harbor
- ArgoCD

---

Last Updated

v2026.07.1 Stable
