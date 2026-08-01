# Microservices-Task

## Overview
This document provides details on testing various services after running the `docker-compose` file. These services include User, Product, Order, and Gateway Services. Each service has its own endpoints for testing purposes.

---
## Creating Dockerfile for each services and docker compose for all create and call together

### **User Service Dockerfile**

 - **Step 1:** Creating Dockerfile for users service

 - <img width="746" height="69" alt="image" src="https://github.com/user-attachments/assets/0316f160-dbd9-41b4-ae3a-70383b43b7a8" />

 - <img width="746" height="280" alt="image" src="https://github.com/user-attachments/assets/5697db28-7fa1-4afc-bc5c-3ea8cb751a42" />

- **Step 2:** Commit and Push Dockerfile into github

- <img width="746" height="847" alt="image" src="https://github.com/user-attachments/assets/711fc74f-08c0-41cd-aa0a-0f224fb32757" />

---

### **Product Service Dockerfile**

- **Step 1:** Creating Dockerfile for Product service

- <img width="746" height="421" alt="image" src="https://github.com/user-attachments/assets/8ac245fd-ea86-40bf-854b-b1c63ad55477" />

- **Step 2:** Commit and Push Dockerfile into github

- <img width="746" height="771" alt="image" src="https://github.com/user-attachments/assets/5a0552c5-d3c9-4e33-9567-5fa91831960f" />

---

### **Order Service Dockerfile**

- **Step 1:** Creating Dockerfile for Order service

- <img width="746" height="483" alt="image" src="https://github.com/user-attachments/assets/c033ab37-1a66-4369-b55f-673ce19ce32a" />

- **Step 2:** Commit and Push Dockerfile into github

- <img width="746" height="783" alt="image" src="https://github.com/user-attachments/assets/a7c24064-379e-4a61-bcb4-7d357dad9146" />

---

### **Gateway Service Dockerfile**

- **Step 1:** Creating Dockerfile for Gateway service

- <img width="746" height="476" alt="image" src="https://github.com/user-attachments/assets/5c568598-27b6-4307-b178-ccc0236f570b" />

- **Step 2:** Commit and Push Dockerfile into github

- <img width="746" height="749" alt="image" src="https://github.com/user-attachments/assets/24747336-7a50-4b9e-bb04-4e292173a1d8" />

---

## Creating Docker compose file 

- **Step 1:** Creating Docker Compose file

- <img width="746" height="933" alt="image" src="https://github.com/user-attachments/assets/1628b651-f8fe-4d86-96c8-2d46f249d210" />

- **Step 2:** Commit and Push Docker Compose file into github

- <img width="746" height="779" alt="image" src="https://github.com/user-attachments/assets/9f0878c3-bb4a-4b49-8aff-463aa708a8f5" />

---

## RUN Docker compose commands to Create image and run docker container

- **Step 1:** Build Images via Docker Compose file

- <img width="1000" height="200" alt="image" src="https://github.com/user-attachments/assets/e92dd435-d4b2-4fa0-9de4-620b42ede98b" />

- <img width="1000" height="200" alt="image" src="https://github.com/user-attachments/assets/47585e24-02ef-440b-a4c2-20733cf3ed71" />

- <img width="1000" height="200" alt="image" src="https://github.com/user-attachments/assets/8f852af0-9e7a-4859-9f78-b6df2d9ee4d6" />

- <img width="1000" height="200" alt="image" src="https://github.com/user-attachments/assets/a56a226e-cee1-44e6-8978-8375fc1284df" />

---

- **Step 2:** Run docker compose

- <img width="746" height="237" alt="image" src="https://github.com/user-attachments/assets/ef97c02c-4396-454c-a8d8-fa2374c557f5" />


- **Step 3:** Check Container is running / check image is created via docker ps/ image command

- <img width="746" height="281" alt="image" src="https://github.com/user-attachments/assets/303bb6df-b3e4-49ab-8e28-44ff0e19f76b" />

---

## Services and Endpoints

### **User Service**
- **Base URL:** `http://localhost:3000`
- **Endpoints:**
  - **List Users:**  
    ```
    curl http://localhost:3000/users

    ```
    - <img width="626" height="81" alt="image" src="https://github.com/user-attachments/assets/b60e61c6-3423-4396-9949-b281aa72b5d5" />
    
    Or open in your browser: [http://localhost:3000/users](http://localhost:3000/users)

    - <img width="626" height="337" alt="image" src="https://github.com/user-attachments/assets/d89343de-afee-4e08-a074-3398a8a7466b" />


---

### **Product Service**
- **Base URL:** `http://localhost:3001`
- **Endpoints:**
  - **List Products:**  
    ```
    curl http://localhost:3001/products
    
    ```
    - <img width="626" height="85" alt="image" src="https://github.com/user-attachments/assets/fddb516f-a03b-4fc2-babf-7baeab17116d" />
    
    Or open in your browser: [http://localhost:3001/products](http://localhost:3001/products)

    - <img width="626" height="351" alt="image" src="https://github.com/user-attachments/assets/f3132f0f-af66-464b-9a5e-cbf081c84175" />

---

### **Order Service**
- **Base URL:** `http://localhost:3002`
- **Endpoints:**
  - **List Orders:**  
    ```
    curl http://localhost:3002/orders    
    ```
    <img width="626" height="93" alt="image" src="https://github.com/user-attachments/assets/dab0d1f8-705e-434f-ae74-f955d6a01104" />

    Or open in your browser: [http://localhost:3002/orders](http://localhost:3002/orders)
    
    - <img width="626" height="174" alt="image" src="https://github.com/user-attachments/assets/aa3173e3-b8a7-4795-ab11-27fd63c4fe3f" />

---

### **Gateway Service**
- **Base URL:** `http://localhost:3003/api`

- <img width="626" height="155" alt="image" src="https://github.com/user-attachments/assets/f53840a3-5e04-4fcf-b516-39b062ed6a5d" />

- **Endpoints:**
  - **Users:**  
    ```
    curl http://localhost:3003/api/users
    ```
     Or open in your browser: http://localhost:3003/api/users [http://localhost:3003/api/users](http://localhost:3003/api/users)

    - <img width="626" height="321" alt="image" src="https://github.com/user-attachments/assets/345d7cc6-dd99-4931-88c8-446cf338c514" />

    
  - **Products:**  
    ```
    curl http://localhost:3003/api/products
    ```
     Or open in your browser: http://localhost:3003/api/users [http://localhost:3003/api/products](http://localhost:3003/api/products)

    - <img width="626" height="357" alt="image" src="https://github.com/user-attachments/assets/a7c763a5-944d-4d24-baca-d6ddcc739dec" />

    
  - **Orders:**  
    ```
    curl http://localhost:3003/api/orders
    ```
     Or open in your browser: http://localhost:3003/api/users [http://localhost:3003/api/orders](http://localhost:3003/api/orders)

    - <img width="626" height="229" alt="image" src="https://github.com/user-attachments/assets/03cd338b-0734-4447-a5fe-a119fc745289" />


---

## Instructions
1. Start all services using the `docker-compose` file:
   ```
   docker-compose up
   ```
   - <img width="626" height="236" alt="image" src="https://github.com/user-attachments/assets/c5a12793-2140-4781-9fcc-072a046f6cd9" />

2. Once the services are running, use the above endpoints to verify the functionality.

Happy testing!
