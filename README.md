# confighub-docker-compose
Docker-compose stack to run ConfigHub service: https://www.confighub.com

# Step's

Create file `.env`

```bash
cp .env.test .env
```

First of all you need create mysql container

```bash
docker-compose up -d mysql
```

After create mysql container, now you need execute migration to populate tables

```bash
docker-compose up -d confighub-db-manager
```

Now, up application

```bash
docker-compose up -d confighub
```

You can access now using URL: http://localhost:8080


More details, please visit: http://docs.confighub.com/en/latest/ & https://github.com/ConfigHubPub
