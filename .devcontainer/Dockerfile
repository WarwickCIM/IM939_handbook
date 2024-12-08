# Start from an official Python base image
FROM python:3.9-slim

# Set the working directory inside the container
WORKDIR /workspace

# Copy the environment.yml file into the container
COPY environment.yml /workspace/

# Install pip, and then install dependencies from the environment.yml file
RUN pip install --upgrade pip \
    && pip install -r /workspace/environment.yml

# Optionally, copy your application code into the container
# COPY . /workspace/

# Expose the port (if you are running a web app, for example)
EXPOSE 5000

# Set the default command to run when the container starts (e.g., a web app)
CMD ["python", "app.py"]
