# CPU and RAM Monitoring with Docker

This project demonstrates a simple system to monitor CPU and RAM usage, send the data to a RabbitMQ queue, and display it on a Flask-based web UI. The project uses Docker and Docker Compose to manage the services.

## Project Structure

project/
│
├── docker-compose.yml
├── cpu_ram_monitor/
│   ├── Dockerfile
│   └── monitor.py
│
├── rabbitmq/
│   ├── Dockerfile
│
└── flask_ui/
    ├── Dockerfile
    ├── app.py
    └── templates/
        └── index.html


## Services

1. **cpu_ram_monitor**: This service collects CPU and RAM usage data every 5 seconds and sends it to RabbitMQ.
2. **rabbitmq**: This service runs a RabbitMQ instance to handle message queuing.
3. **flask_ui**: This service runs a Flask web application to display the collected data.

## How to Run

1. Make sure you have Docker and Docker Compose installed.
2. Clone this repository:
   ## bash
   git clone https://github.com/YOUR_USERNAME/cpu_ram_monitoring.git
   cd cpu_ram_monitoring


## Build and start the services
docker-compose up --build

## Open your browser and go to http://localhost:5000 to see the CPU and RAM usage.

## Note
The cpu_ram_monitor and flask_ui services will retry connection to RabbitMQ every 5 seconds if the connection fails.