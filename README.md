
# DevOps Internship Project

This project demonstrates deploying two microservices using Docker and Docker Compose, routed through an NGINX reverse proxy.

---

## 🧱 Tech Stack

- 🔵 Golang (Service 1)
- 🐍 Python Flask (Service 2)
- 🌐 NGINX (Reverse Proxy)
- 🐳 Docker & Docker Compose

---

## 📁 Folder Structure

```
devops-internship-project/
│
├── service_1/             # Golang service
│   ├── main.go
│   └── Dockerfile
│
├── service_2/             # Python service (Flask)
│   ├── app.py
│   └── Dockerfile
│
├── nginx/                 # NGINX reverse proxy config
│   ├── nginx.conf
│   └── Dockerfile
│
├── docker-compose.yml
└── README.md
```

---

## ⚙️ How to Run the Project

### 1. Open the Project Folder

```bash
cd path/to/devops-internship-project
```

### 2. Build the Docker Images

```bash
docker-compose build --no-cache
```

### 3. Start the Services

```bash
docker-compose up
```

### 4. Test the Endpoints

✅ Service 1 (Golang):  
[http://localhost:8080/service1/ping](http://localhost:8080/service1/ping)

✅ Service 2 (Python Flask):  
[http://localhost:8080/service2/hello](http://localhost:8080/service2/hello)

### 5. Stop and Clean Up

```bash
docker-compose down
```

---

## 📌 Notes

- Make sure Docker is running before you start.
- NGINX listens on port `8080` and routes requests to:
  - `/service1/` → Golang service on port `8001`
  - `/service2/` → Python service on port `8002`

---

## 📬 Author

Kalyan Nagapuri  
GitHub: [https://github.com/kalyan3759](https://github.com/kalyan3759)
