FROM python:3.8-slim

# Install dependencies
RUN pip install pika psutil flake8 pytest coverage

# Set the working directory
WORKDIR /app

# Copy the current directory contents into the container
COPY . .

# Run monitor.py
CMD ["python", "monitor.py"]
