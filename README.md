# Big Data Analytics Platform: Distributed E-Commerce Intelligence Warehouse

This repository implements a distributed big data processing architecture utilizing MongoDB, Apache HBase, and Apache Spark (PySpark) to ingest, store, clean, and analyze complex multi-system e-commerce data.

## Step-by-Step Instructions to Reproduce Results

### 1. Spin up the Database Infrastructure Layer
Ensure Docker Desktop is active on your machine. Open a  PowerShell window in this directory and execute:
```powershell
docker compose up -d
```

### 2. Open up the connection port for HappyBase
```powershell
docker exec -d local-hbase hbase thrift start
```

### 3. Run Distributed Analytics and SQL Cross-Joins
Execute the PySpark processing engine to generate affinity matrices and cross-database joins:
```powershell
python spark_analytics.py
python integration_analytics.py
python generate_plots.py
```

