# Spring Boot Docker Demo

A simple Spring Boot application deployed with Docker.

---

## 🧩 Steps to Run

### 1️⃣ Build the JAR
```bash
.\mvnw.cmd clean package
```

### 2️⃣ Build the Docker Image
```bash
docker build -t springboot-demo .
```

### 3️⃣ Run the Container
```bash
docker run -p 8080:8080 springboot-demo
```

Then open your browser and go to:  
👉 [http://localhost:8080](http://localhost:8080)

You should see:
> **Hello from Spring Boot on Kubernetes!**

---

## 🐳 Dockerfile
```dockerfile
FROM eclipse-temurin:17-jdk-alpine
WORKDIR /app
COPY target/demo-0.0.1-SNAPSHOT.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "app.jar"]
```
