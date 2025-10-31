# MUHAMMAD AZIM BIN AZLI

# 🌐 Web Application Load Testing with Vegeta 🔥

<img width="700" alt="image" src="https://github.com/user-attachments/assets/0760177f-6683-4f3f-90e1-6bfb18941c04" />

---

# 📋 Assignment Details
- **Course:** ITT440
- **Name:** MUHAMMAD AZIM AZLI  
- **Matrix Number:** 2024539875
- **Tool Used:** Vegeta v12.12.0  
- **Target Website:** [https://blazedemo.com/](https://blazedemo.com/)  
- **YouTube Video:** *(Insert Link Here)*

---

# 📱 Introduction
This project demonstrates a **30-second load test** and **50-request per second load test** on BlazeDemo using the **Vegeta load testing tool**.  
Load testing helps evaluate the **server’s performance, reliability, and responsiveness** under simulated user traffic.

---

# ⚙️ Test Environment & Methodology
## Test Setup
- **Tool:** Vegeta v12.12.0  
- **Rate:** 50 requests per second  
- **Duration:** 30 seconds  
- **Test Type:** Load Test (Performance & Stability)  
- **Target Website:** BlazeDemo  
- **Total Requests:** ~1500  

## Metrics Tracked
- Requests per second  
- Latencies (min, mean, percentiles, max)  
- Throughput rate  
- Success ratio  
- Status code  
- Error set  

---
# ⏱ Test Execution

## Vegeta Commands
```bash
# Open the cmd or powerShell in administration mode first and enter the directory
cd C:\Users\HP\Documents\vegeta_12.12.0_windows_amd64

# Create target file
Set-Content -Encoding Ascii targets.txt "GET https://blazedemo.com/"

# Run Vegeta attack (30 seconds at 50 requests/sec)
& .\vegeta.exe attack -duration 30s -rate 50 -targets targets.txt -output results.bin

# Generate test report
cmd /c ".\vegeta.exe report < results.bin"

# Create HTML plot
cmd /c ".\vegeta.exe plot < results.bin > plot.html"

# Open the HTML visualization
Start-Process plot.html
---



