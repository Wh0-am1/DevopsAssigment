### 🧪 **DevOps Intern Assignment: Nginx Reverse Proxy + Docker**

1. **Two Dockerized backend services** (can be dummy services) run on different ports.
2. An **Nginx reverse proxy** (also in a Docker container) routes:

   - `/service1` requests to backend service 1
   - `/service2` requests to backend service 2

3. All services must be accessible via a single port `localhost:8080`.

---

1. Use Docker Compose to bring up the entire system.
2. Each backend service should respond with a JSON payload like:

   ```json
   { "service": "service1" }
   ```

3. The Nginx config should support:

   - Routing based on URL path prefix (`/service1`, `/service2`)
   - Logging incoming requests with timestamp and path

4. The system should work with a single command:

   ```bash
   docker-compose up --build
   ```

5. Bonus: health check for both services and show logs of successful routing.

```bash
  docker ps
```

- check with the above command

---

### 📁 Project Structure

```
.
├── docker-compose.yml
├── nginx
│   ├── default.conf
│   └── Dockerfile
├── service_1
│   ├── app.py
│   └── Dockerfile
├── service_2
│   ├── app.py
│   └── Dockerfile
└── README.md
```

---

## Extra

- proxy_set_header
