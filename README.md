# SimpleTimeService

A minimal Flask-based microservice that returns the current UTC timestamp and the IP address of the client in JSON format.

## 🔧 Features

- Returns current timestamp in ISO 8601 format
- Shows IP address of the requester
- Lightweight container image using Python 3.11-slim
- Runs as a **non-root user**

---

## 🚀 How to Deploy

### 1. Clone the repository

```bash
git clone https://github.com/riddhigala09/SimpleTimeService.git
```
``` bash
cd SimpleTimeService
```

### 2. Pull and run the Docker image

```bash
docker pull riddhigala18/simple-time-service:latest
```
``` bash
docker run -d -p 5000:5000 simple-time-service:latest 
```
### 3. Test the service

```bash
curl http://localhost:5000/
```
Expected response:
```json
{
    "ip":"172.17.0.1",
    "timestamp":"2025-07-14T06:00:29.333965Z"
}
```
