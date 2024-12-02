FROM ubuntu

WORKDIR /app

# Copy the requirements and devops folder into the container
COPY requirements.txt /app
COPY devops /app

# Install necessary dependencies and Python, then install Python packages
RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    python3 -m pip install --upgrade pip && \  # Update pip to avoid potential issues with old versions
    pip install -r requirements.txt

# Set environment variables for the container to use the virtual environment (if needed)
# This step may not be necessary, depending on your app setup

# Define the default command to run the Django development server
ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]





