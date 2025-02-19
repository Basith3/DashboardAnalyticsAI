# .NET Core Backend API

## 📌 Overview
This is a **.NET Core Web API** project built using **ASP.NET Core 9.0**. It serves as the backend for a scalable application that integrates with **Elasticsearch, LiteDB, and PostgreSQL**. The API is containerized with **Docker** and deployable to **AWS ECS**.

## 🚀 Features
- RESTful API architecture
- Database support for PostgreSQL, Elasticsearch, and LiteDB
- Integrated **Serilog** logging
- Dependency Injection (DI) for modular services
- Containerized with **Docker**
- Scalability with **Nginx Load Balancing**

## 🛠️ Tech Stack
- **Backend:** ASP.NET Core 7.0 (C#)
- **Database:** PostgreSQL, LiteDB, Elasticsearch
- **Logging:** Serilog
- **Deployment:** Docker, AWS ECS
- **Reverse Proxy:** Nginx

## 📂 Folder Structure
```
backend/
│── Controllers/    # API controllers
│── Models/         # Data models
│── Services/       # Business logic services
│── Data/           # Database context & repositories
│── Logging/        # Logging setup (Serilog)
│── appsettings.json # Configurations
│── Program.cs      # Entry point
│── Startup.cs      # Middleware & DI setup
│── Dockerfile      # Docker container setup
│── README.md       # Documentation
```

## 🏗️ Setup & Installation
### 1️⃣ Prerequisites
- Install **.NET SDK 9.0**
- Install **Docker** (if deploying with containers)
- Install **PostgreSQL** & **Elasticsearch** (for data storage)

### 2️⃣ Clone Repository
```sh
git clone https://github.com/your-repo/backend.git
cd backend
```

### 3️⃣ Install Dependencies
```sh
dotnet restore
```

### 4️⃣ Run the API Locally
```sh
dotnet run
```
The API will start at `http://localhost:5000`

### 5️⃣ Build & Run with Docker
# .NET Core Backend API

## 📌 Overview
This is a **.NET Core Web API** project built using **ASP.NET Core 7.0**. It serves as the backend for a scalable application that integrates with **Elasticsearch, LiteDB, and PostgreSQL**. The API is containerized with **Docker** and deployable to **AWS ECS**.

## 🚀 Features
- RESTful API architecture
- Database support for PostgreSQL, Elasticsearch, and LiteDB
- Integrated **Serilog** logging
- Dependency Injection (DI) for modular services
- Containerized with **Docker**
- Scalability with **Nginx Load Balancing**
- AI Service for data processing
- Monitoring with **Prometheus & Grafana**

## 🛠️ Tech Stack
- **Backend:** ASP.NET Core 7.0 (C#)
- **Frontend:** Angular
- **Database:** PostgreSQL, LiteDB, Elasticsearch
- **Logging:** Serilog
- **Deployment:** Docker, AWS ECS
- **Reverse Proxy:** Nginx
- **Monitoring:** Prometheus & Grafana

## 📂 Folder Structure
```
backend/
│── Controllers/    # API controllers
│── Models/         # Data models
│── Services/       # Business logic services
│── Data/           # Database context & repositories
│── Logging/        # Logging setup (Serilog)
│── appsettings.json # Configurations
│── Program.cs      # Entry point
│── Startup.cs      # Middleware & DI setup
│── Dockerfile      # Docker container setup
│── README.md       # Documentation
nginx/
│── nginx.conf      # Nginx reverse proxy config
prometheus/
│── prometheus.yml  # Prometheus configuration
```

## 🏗️ Setup & Installation
### 1️⃣ Prerequisites
- Install **.NET SDK 7.0**
- Install **Docker**
- Install **PostgreSQL** & **Elasticsearch**

### 2️⃣ Clone Repository
```sh
git clone https://github.com/your-repo/backend.git
cd backend
```

### 3️⃣ Install Dependencies
```sh
dotnet restore
```

### 4️⃣ Run the API Locally
```sh
dotnet run
```
The API will start at `http://localhost:5000`

### 5️⃣ Build & Run with Docker Compose
```sh
docker-compose up --build
```

## 📌 Services & Endpoints
| Service        | Endpoint                          | Description            |
|---------------|---------------------------------|------------------------|
| Backend API   | `http://localhost:5000`         | .NET API service       |
| Frontend      | `http://localhost:4200`         | Angular UI             |
| AI Service    | `http://localhost:8000`         | FastAPI AI processing  |
| PostgreSQL    | `localhost:5432`                | SQL Database           |
| Elasticsearch | `http://localhost:9200`         | NoSQL Data Store       |
| Nginx         | `http://localhost`              | Reverse Proxy          |
| Prometheus    | `http://localhost:9090`         | Monitoring             |
| Grafana       | `http://localhost:3000`         | Visualization          |


## 📌 API Endpoints
| Method | Endpoint       | Description          |
|--------|--------------|----------------------|
| GET    | `/api/health` | Check API health    |
| GET    | `/api/data`   | Fetch data          |
| POST   | `/api/data`   | Insert data         |

## 🔧 Environment Variables
Create an `.env` file:
```
DB_CONNECTION_STRING=Server=localhost;Database=postgres;User=postgres;Password=secret
ELASTICSEARCH_URL=http://localhost:9200
LITEDB_PATH=./Data/lite.db
```

## 🏗️ Deployment to AWS ECS
1. Build and push Docker image:
```sh
docker build -t backend-api .
docker tag backend-api:latest <AWS_ECR_URL>/backend-api:latest
docker push <AWS_ECR_URL>/backend-api:latest
```
2. Deploy using Terraform (refer `deployment/terraform/main.tf`)
```sh
terraform init
terraform apply -auto-approve
```

## 🔍 Monitoring with Grafana & Prometheus
- Expose metrics at `/metrics`
- Use Prometheus + Grafana for API monitoring

## 📜 License
MIT License © 2025 AbdulBasithMohamed

