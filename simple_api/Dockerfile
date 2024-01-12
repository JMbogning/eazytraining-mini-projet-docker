# Use the base image
FROM python:3

# Specify maintainer information
LABEL Junior Mbogning <juniormbogning@gmail.com>

# Set the working directory
WORKDIR /

# Copy the source code of the API to the container
COPY student_age.py /

# Install prerequisites
RUN apt update -y && apt install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y \
    && pip install flask==1.1.2 flask_httpauth==4.1.0 flask_simpleldap python-dotenv==0.14.0

# Create a data folder and declare it as a volume
VOLUME /data

# Expose port 5000
EXPOSE 5000

# Set CMD to run student_age.py when the container starts
CMD ["python", "./student_age.py"]
