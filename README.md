# Kaiburr Task 2 - Kubernetes Deployment

    This repository contains my implementation of **Task 2** for Kaiburr’s assessment — deploying the Java Spring Boot backend and MongoDB in a Kubernetes environment.

---

## 📁 Project Overview

    - **Backend**: Java Spring Boot application
    - **Database**: MongoDB
    - **Features**:
        - Deploys MongoDB with PersistentVolume (PV) and PersistentVolumeClaim (PVC)
        - Deploys the Java Spring Boot backend app
        - Exposes the backend app via NodePort service

---

## 🚀 Deployment Steps

    ✅ **1️⃣ Start Minikube:**
    ```bash
    minikube start
    ```

    ✅ **2️⃣ Deploy MongoDB PV & PVC:**
    ```bash
    kubectl apply -f k8s/mongo-pv.yaml
    ```

    ✅ **3️⃣ Deploy MongoDB:**
    ```bash
    kubectl apply -f k8s/mongo-deployment.yaml
    ```

    ✅ **4️⃣ Deploy MongoDB Service:**
    ```bash
    kubectl apply -f k8s/mongo-service.yaml
    ```

    ✅ **5️⃣ Deploy the Java backend app:**
    ```bash
    kubectl apply -f k8s/app-deployment.yaml
    ```

    ✅ **6️⃣ Expose the backend app using NodePort service:**
    ```bash
    kubectl apply -f k8s/app-service.yaml
    ```

    ✅ **7️⃣ Verify deployments:**
    ```bash
    kubectl get pods
    kubectl get svc
    ```

    ✅ **8️⃣ (Optional) Port-forward to access the app locally:**
    ```bash
    kubectl port-forward pod/<task-api-pod-name> 8080:8080
    ```

---

## 📦 Endpoints

    ✅ Access the API using:

    ```
    http://<minikube_ip>:30080/tasks
    ```

    👉 Get Minikube IP:
    ```bash
    minikube ip
    ```

---

## 📸 Screenshots

    All screenshots are saved in the `screenshots/` folder:

    ✅ `kubectl get pods`  
    ✅ `kubectl get svc`  
    ✅ API in browser  

---

## ⚠️ Note

    ❌ Due to MongoDB connection issues in my environment, the backend app may not display tasks as expected.  
    ✅ However, all Kubernetes resources were deployed and verified.

---

## ✅ Task 2 Complete!

    Thank you for the opportunity to complete this task!

---

**Author:** Dhanish  
**Date:** 2025
