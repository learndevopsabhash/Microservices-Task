# Skill Test 2: Container Orchestration on Microservices-Task

## Overview
This document provides details on testing various services kubernets deployment and service files. 
These Kubernets Deployment and services include User, Product, Order, and Gateway Services. Each service has its own endpoints for testing purposes.

---

## Project Architecture

```
Microservices
│
├── deployments
│   ├── user-service.yaml
│   ├── product-service.yaml
│   ├── order-service.yaml
│   └── gateway-service.yaml
│
├── services
│   ├── user-service.yaml
│   ├── product-service.yaml
│   ├── order-service.yaml
│   └── gateway-service.yaml
│
├── ingress
│   └── ingress.yaml
|
├── gateway-service/
│   ├── Dockerfile
│   ├── app.js
│   └── package.json
├── order-service/
│   ├── Dockerfile
│   ├── app.js
│   └── package.json
├── product-service/
│   ├── Dockerfile
│   ├── app.js
│   └── package.json
├── user-service/
│   ├── Dockerfile
│   ├── app.js
│   └── package.json
|
├── docker-compose.yml
|
└── README_Skill_Test_2.md
|
└── README.md
```


## Setup code form Github

### Step 1 - Clone git repo

git clone https://github.com/learndevopsabhash/Microservices-Task.git

<img width="900" height="170" alt="image" src="https://github.com/user-attachments/assets/f92c034d-c09b-4ee1-9bf7-7b9015fb11f5" />

cd Microservices

ll

<img width="825" height="187" alt="image" src="https://github.com/user-attachments/assets/7dd74a26-b75a-4b6f-9fc8-9762c0d35955" />


### Step 2 - Creating folder structure for Kubernetes Deployment manifests

<img width="832" height="125" alt="image" src="https://github.com/user-attachments/assets/eeeb3da2-4c46-4d00-9895-f18775f39303" />


## Build Docker Images for kubernets deployments

cd Microservices

Run command to create docker image for user-service - docker build -t user-service:v1 ./user-service

<img width="1140" height="625" alt="image" src="https://github.com/user-attachments/assets/12694c44-7a11-4a3b-bb8e-00c73b9a6227" />

Run command to create docker image for product-service - docker build -t product-service:v1 ./product-service

<img width="1107" height="682" alt="image" src="https://github.com/user-attachments/assets/575acb96-c905-4b51-a003-acdca85509b1" />

Run command to create docker image for order-service - docker build -t order-service:v1 ./order-service

<img width="1101" height="625" alt="image" src="https://github.com/user-attachments/assets/65f5fd46-ceb6-4c8c-b724-e829f1e40fb3" />

Run command to create docker image for gateway-service - docker build -t gateway-service:v1 ./gateway-service

<img width="1105" height="578" alt="image" src="https://github.com/user-attachments/assets/f5f8307c-ed16-4ecd-a65d-321cfd29e32c" />


<img width="1533" height="207" alt="image" src="https://github.com/user-attachments/assets/c6bdc592-da61-473a-8141-dd8d2e3600df" />


## Start Minikube and Load Docker Images

<img width="1037" height="388" alt="image" src="https://github.com/user-attachments/assets/2d15b739-7caf-4d27-95ae-245e303dcdb1" />


## Push image to minikube

<img width="825" height="62" alt="image" src="https://github.com/user-attachments/assets/e6aee150-cacc-42b5-9b86-f4d25a945730" />

<img width="827" height="190" alt="image" src="https://github.com/user-attachments/assets/50be58fe-5175-4553-adea-c54315b17433" />


<img width="850" height="345" alt="image" src="https://github.com/user-attachments/assets/e37a1907-e89f-4799-a57e-7cb6fbce2f24" />


## Create Kubernetes Deployment manifests files for all services

### For Deployment

<img width="961" height="397" alt="image" src="https://github.com/user-attachments/assets/bcef5207-ddfa-445c-a97b-3d8195fd86c1" />

### for services

<img width="917" height="262" alt="image" src="https://github.com/user-attachments/assets/ebbc9319-1797-4110-ab57-4e613be03354" />

## Deploy the Microservices to Kubernetes

### Deploy the Deployments 

<img width="867" height="140" alt="image" src="https://github.com/user-attachments/assets/a4946341-93ab-4e3e-a00f-6384cc437696" />

### Deploy the Services

<img width="846" height="152" alt="image" src="https://github.com/user-attachments/assets/49ae5685-7167-42da-b5a4-28810207a09e" />

### Verify pods 

<img width="831" height="240" alt="image" src="https://github.com/user-attachments/assets/362a3855-c999-45e1-bad5-a73c029e81a1" />

### Verify Deployments

<img width="826" height="193" alt="image" src="https://github.com/user-attachments/assets/03d549a1-67e8-4c3e-a224-0a88b89bd9bb" />

### Verify Services

<img width="912" height="225" alt="image" src="https://github.com/user-attachments/assets/1b38fb6e-dc37-4a57-9390-22f50c50c1e1" />


### Verify Pod Health

<img width="986" height="631" alt="image" src="https://github.com/user-attachments/assets/3519a013-359e-4275-8780-1d28bf138419" />



## Validate Inter-Service Communication and Test the Application

### Start Port Forwarding

The Gateway Service is a ClusterIP service, which means it is only accessible from inside the Kubernetes cluster so we need to port forwarding.

<img width="908" height="172" alt="image" src="https://github.com/user-attachments/assets/d3eb4a16-c74b-4677-a2fe-f26b70f06683" />

### Test Gateway Health

<img width="418" height="175" alt="image" src="https://github.com/user-attachments/assets/a3ad3933-6992-4e40-bc97-2e4c8c342900" />

### Test User Service Through Gateway

<img width="565" height="247" alt="image" src="https://github.com/user-attachments/assets/4484be69-9b54-4d49-8687-2c0fd980a194" />

### Test Product Service Through Gateway

<img width="472" height="292" alt="image" src="https://github.com/user-attachments/assets/78654ea3-664d-45e9-99e0-bff1b40e3dd9" />

### Test Order Service

<img width="455" height="208" alt="image" src="https://github.com/user-attachments/assets/7ddcd0f8-6076-4c0c-ba90-9de4fbb391d9" />

### Create a New Order

<img width="833" height="160" alt="image" src="https://github.com/user-attachments/assets/3e97dd3e-2f7a-4645-b91f-62b2813a5b70" />

<img width="517" height="317" alt="image" src="https://github.com/user-attachments/assets/97e3964f-0dd3-4740-925a-a502e9272f78" />

### View Application Logs

<img width="827" height="347" alt="image" src="https://github.com/user-attachments/assets/302409e9-1cce-4dec-99ca-144d9b71e882" />


## Ingress Configuration 
A Kubernetes **Ingress** is an API object that manages external HTTP and HTTPS access to services within a cluster.
Instead of exposing each service individually, Ingress acts as a single entry point and routes requests to different services based on URL paths or hostnames.
 
### Enable the Ingress Controller

<img width="1170" height="335" alt="image" src="https://github.com/user-attachments/assets/0fafe291-6eff-43b3-9ba8-c7e32fa5d403" />

<img width="1022" height="137" alt="image" src="https://github.com/user-attachments/assets/f5e337b3-4cbd-4b3f-a97c-4d8b65362721" />

### Create the Ingress Directory

<img width="825" height="120" alt="image" src="https://github.com/user-attachments/assets/126dab47-6aaf-458b-8b88-07cadf734517" />

### Create ingress/ingress.yaml

<img width="822" height="122" alt="image" src="https://github.com/user-attachments/assets/6b0b898b-7d1c-47af-913d-c78e8641a7e3" />


### Apply the Ingress

- kubectl apply -f ingress/

<img width="835" height="86" alt="image" src="https://github.com/user-attachments/assets/98e988c1-c518-44c5-a710-ae8582b320f8" />

### Veryfy ingress service

<img width="822" height="115" alt="image" src="https://github.com/user-attachments/assets/08ec7fdd-4816-45c1-8a03-7c16566ee6e5" />

### Test the Ingress
1. check minikube IP

   <img width="547" height="67" alt="image" src="https://github.com/user-attachments/assets/065d2313-0a78-42b7-99c4-044d2480eb72" />

2. Add an entry to your hosts file in windows > C:\Windows\System32\drivers\etc\hosts
   
   <img width="307" height="97" alt="image" src="https://github.com/user-attachments/assets/fc307e55-5426-454a-a721-8d9edc3bb376" />

---

## Instructions
1. Start all services using the `Kubernets`:
   ```
   ```
2. Once the services are running, use the above endpoints to verify the functionality.

Happy testing!
