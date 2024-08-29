# Use the latest Ubuntu as the base image
FROM ubuntu:latest

# Update APT and upgrade packages
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Remove the EXTERNALLY-MANAGED file if it exists
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip3
RUN pip3 install flask flask-cors

# Set the working directory
WORKDIR /app

# Copy the api.py file into the container
COPY ./api.py /app/api.py

# Expose the port that the Flask app will run on
EXPOSE 5252

# Set the command to run the Flask server
CMD ["python3", "api.py"]
