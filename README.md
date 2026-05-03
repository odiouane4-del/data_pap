# data_paprealtime-weather-pipeline/
├── docker-compose.yml          ← 7 services orchestrated
├── Dockerfile.producer         ← Lightweight Python image
├── Dockerfile.spark            ← Bitnami Spark 3.5 + pre-loaded JARs
├── weather_producer.py         ← OWM → Kafka (10 cities, every 10s)
├── spark_processor.py          ← Kafka → PySpark → PostgreSQL
├── sql/
│   └── database_schema.sql     ← 3 tables, 8 indexes, 2 views, 1 procedure
├── config/
│   └── grafana_datasource.yml  ← Auto-provisions WeatherDB in Grafana
├── requirements.txt
├── .env.example
└── .gitignore
