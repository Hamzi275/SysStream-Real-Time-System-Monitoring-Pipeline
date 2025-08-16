# 🔥 SysStream-Real-Time-System-Monitoring-Pipeline
SysStream is a real-time monitoring pipeline that captures CPU, memory, disk, and network metrics, streams them via Apache Kafka, stores them in SQL Server, and visualizes insights in Power BI. It demonstrates scalable data engineering with live system performance analytics.
This project is a **real-time monitoring pipeline** that captures **system performance metrics** (CPU, Memory, Disk, Network usage), streams them via **Apache Kafka**, stores them in **SQL Server**, and finally visualizes them in a **Power BI Dashboard**.  

The main goal of this project is to provide **live system insights** using a scalable data pipeline and interactive visualization.

---

## ⚙️ Project Architecture
1. **Producer (Python + psutil):**
   - Captures system performance metrics such as CPU usage, memory usage, disk usage, and network traffic.
   - Sends this data to a Kafka topic in real-time.

2. **Kafka Broker:**
   - Acts as the streaming backbone of the project.
   - Receives data from the producer and makes it available for consumers.

3. **Consumer (Python + pyodbc):**
   - Listens to Kafka topic messages.
   - Inserts the performance metrics into a SQL Server database (`Performance` table).

4. **SQL Server:**
   - Stores all the system performance metrics.
   - Serves as the backend database for Power BI.

5. **Power BI Dashboard:**
   - Connects directly to SQL Server.
   - Provides interactive visualizations for CPU, memory, disk, and network performance.

---

## 🛠️ Tech Stack
- **Python 3.9+**
- **Apache Kafka (Windows)**
- **SQL Server (Express Edition)**
- **Power BI Desktop / Power BI Service**
- **Libraries:** `kafka-python`, `psutil`, `pyodbc`

---



# (Optional) Test Consumer
.\bin\windows\kafka-console-consumer.bat --topic firstTopic --from-beginning --bootstrap-server localhost:9092
