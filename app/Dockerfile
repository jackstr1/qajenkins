# Use Python 3.6 or later as a base image
FROM python:latest
# Copy contents into image
COPY . /tmp 
# Install pip dependencies from requirements
RUN pip install -r /tmp/reqs.txt
# Set YOUR_NAME environment variable
ENV YOUR_NAME=\ja
# Expose the correct port
EXPOSE 5500
#Run application
#CMD [ "python", "/tmp/app.py" ]
# Create an entrypoint
ENTRYPOINT ["python", "/tmp/app.py"]
