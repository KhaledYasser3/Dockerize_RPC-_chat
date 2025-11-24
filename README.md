# RPC Chat Server — Docker Assignment

This project contains a simple Go RPC chat server and client.  
The goal of the assignment is to run the server inside a Docker container, test it using the client, and push the Docker image to Docker Hub.

---

## 📂 Project Files
- `server.go` — RPC server implementation  
- `client.go` — RPC client used for testing the server  
- `Dockerfile` — Docker configuration for building and running the server  

---

## 🛠️ Step 1 — Build Docker Image
Run this inside the project folder:

```bash
docker build -t KhaledYaseer31/rpc-chat-server:new .
````

---

## ▶️ Step 2 — Run the Server in Docker

```bash
docker run --rm -p 1234:1234 --name rpc-chat-server KhaledYaseer31/rpc-chat-server:new
```

* `--rm` removes container after exit
* `-p 1234:1234` maps container port 1234 to host port 1234

Keep this terminal running.

---

## 💬 Step 3 — Run the Client (in another terminal)

```bash
go run client.go
```

This connects to the Dockerized RPC server.

---

## 🔐 Step 4 — Create Docker Hub Access Token

From [https://hub.docker.com](https://hub.docker.com):

1. Go to **Account Settings**
2. Open **Security**
3. Create new **Access Token**
4. Choose **Read, Write, Delete**
5. Copy the token

---

## 🔑 Step 5 — Login to Docker Hub from Terminal

```bash
docker login -u khaledyasser31
```

Use the **Access Token** as your password.

---

## 🚀 Step 6 — Tag Image with Correct Docker Hub Username

```bash
docker tag KhaledYaseer31/rpc-chat-server:new khaledyasser31/rpc-chat-server:new
```

---

## 📤 Step 7 — Push Image to Docker Hub

```bash
docker push khaledyasser31/rpc-chat-server:new
```

---

## 🌐 Docker Hub Link

Your pushed image:

[https://hub.docker.com/r/khaledyasser31/rpc-chat-server](https://hub.docker.com/r/khaledyasser31/rpc-chat-server)

---

## ▶️ How to Run the Server (from Docker Hub)

```bash
docker pull khaledyasser31/rpc-chat-server:new
docker run --rm -p 1234:1234 khaledyasser31/rpc-chat-server:new
```

---

## ▶️ How to Run the Client

```bash
go run client.go
```

قولّي الشكل اللي تفضّله وأنا أبعتلك الملف فورًا ❤️
```
