# Taskboard

A todo app with image uploads. Built with Node.js, MongoDB, and Docker.

## Stack

- Node.js + Express
- MongoDB + Mongo Express
- Multer (file uploads)
- Docker + Docker Compose

## Run

```bash
docker build -t todo-app:1.0 .
docker compose up -d
```

| Service       | URL                       |
|---------------|---------------------------|
| App           | http://localhost:3000     |
| Mongo Express | http://localhost:8081     |

## Commands

```bash
docker ps                          # running containers
docker compose logs -f todo-app    # live logs
docker compose down                # stop everything
docker build -t todo-app:1.0 .     # rebuild after changes
```

## Notes

- MongoDB credentials: `admin` / `password`
- App connects to MongoDB via `mongodb:27017` (not localhost)
- Data is lost on container restart — add a volume to persist it
