# Week 6 Advance ADF

## 🔖 Tech Highlights

![ADF](https://img.shields.io/badge/Azure--Data--Factory-ADF-blue)
![AzureSQL](https://img.shields.io/badge/Azure--SQL--Database-blueviolet)
![IncrementalLoad](https://img.shields.io/badge/Incremental--Load-green)
![RetryLogic](https://img.shields.io/badge/Retry--Logic-yellow)
![LastSaturdayTrigger](https://img.shields.io/badge/Last--Saturday--Trigger-critical)
![SHIR](https://img.shields.io/badge/Self--Hosted--IR-important)

---

This repository contains various advanced Azure Data Factory (ADF) pipelines demonstrating real-world integration use cases, automation, and data engineering best practices.

---

## 📌 Completed Tasks

---

## ✅ Task 1: Load Data from Local SQL Server to Azure SQL using SHIR

🔹 Uses Self-hosted Integration Runtime to securely connect on-prem to Azure  
🔹 Copy data from local SQL to Azure SQL table

## ✅ Task 2: Incremental Load Pipeline (with Watermark Logic)

🔹 Incrementally loads only new records from the `Customers` table using `id` as watermark  
🔹 Retrieves last loaded ID from watermark table  
🔹 Uses dynamic SQL with parameterized query

## ✅ Task 3: Automate Daily Runs with Trigger

🔹 Pipeline is triggered **daily**  
🔹 Internally uses `IfCondition` activity to run **only on the last Saturday of the month**

## ✅ Task 4: Retry Logic for Fault Tolerance

🔹 The `Copy` activity is configured with retry policy:
  - Retries: 3
  - Retry Interval: 60 seconds  
🔹 Helps auto-recover from transient failures
