# Use the official Python image from the Docker Hub
FROM python:3.9

# Expose the application port
EXPOSE 8080

# Set environment variables
ENV AMQP_USER=roboshop \
    AMQP_PASS=roboshop123

# Set the working directory
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt /app/

# Install the Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application code and configuration file into the container
COPY *.py /app/
COPY payment.ini /app/

# Run the application using uwsgi
CMD ["uwsgi", "--ini", "payment.ini"]
