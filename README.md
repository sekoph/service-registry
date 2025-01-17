# Spring Boot Service Registry using Eureka

## 📌 Introduction
This project is a **Service Registry** using **Eureka Server** in a **Spring Boot** microservices architecture. Eureka acts as a discovery server where different microservices register themselves and discover other services dynamically.

## 🚀 Features
- Centralized **service registry** for microservices
- Dynamic service discovery
- Load balancing with Eureka clients
- Health check monitoring

## 🛠️ Prerequisites
Ensure you have the following installed:
- **Java 17+**
- **Maven 3.6+**
- **Spring Boot 3+**

## 📂 Project Structure
```
service-registry/
│── src/
│   ├── main/
│   │   ├── java/com/example/serviceregistry/
│   │   │   ├── ServiceRegistryApplication.java
│   │   ├── resources/
│   │       ├── application.yml
│── pom.xml
│── README.md
```

## 🔧 Setup & Configuration

### 1️⃣ Clone the Repository
```sh
git clone git@github.com:sekoph/service-registry.git
cd service-registry
```

### 2️⃣ Add Dependencies to `pom.xml`
Ensure you have the necessary dependencies:
```xml
<dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-starter-netflix-eureka-server</artifactId>
</dependency>
```

### 3️⃣ Configure `application.properties` in resources
```yaml
spring.application.name=service-registry

server.port=8761

eureka.instance.hostname=localhost
eureka.client.fetch-registry=false
eureka.client.register-with-eureka=false
```



### 5️⃣ Run the Eureka Server
```sh
mvn spring-boot:run
```

### 6️⃣ Access Eureka Dashboard
Open your browser and navigate to:
```
http://localhost:8761
```


## 🎯 Testing Service Discovery
1. Start Eureka Server
2. Run microservices with Eureka clients
3. Check Eureka Dashboard at `http://localhost:8761`
4. See registered services under **Instances currently registered with Eureka**

## 📜 License
This project is licensed under the **MIT License**.

## 🤝 Contributing
Pull requests are welcome! Feel free to fork and improve the project.

---
🚀 Happy Coding!

