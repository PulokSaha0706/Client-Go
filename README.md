# 📘 Book API Deployment with Kubernetes Client-Go

This project demonstrates how to deploy a Go-based Book API to Kubernetes using the `client-go` library (no YAML).

---

##  Getting Started

### Clone & Build

Make sure you’ve already built and pushed your Docker image to Docker Hub:

```bash
docker build -t puloksaha/bookapi:latest .
docker push puloksaha/bookapi:latest
```


### Run the Deployment with client-go

Deploy your API programmatically using:
```bash
go run main.go
```
This creates a Kubernetes Deployment with your Docker image and exposes port 9090.

### Port Forward to Access the API

Forward the container port to your local machine:
```bash
kubectl port-forward deployment/bookapi-deployment 9090:9090
```
Now your API is available at:
```bash
http://localhost:9090
```
