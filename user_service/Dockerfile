FROM python:3.9-slim
#set the working directory in the container
WORKDIR /app

#copy the service file and the required dependency files
COPY user_service.py /app/user_service.py

#install pip requirements
COPY requirements.txt /app/requirements.txt

#install pip requirements
RUN pip install fastapi uvicorn

#export the port used by the application
EXPOSE 8002

#command to run the service
CMD ["uvicorn", "user_service:app", "--host", "0.0.0.0", "--port", "8002"]