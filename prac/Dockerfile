FROM python:3.6
COPY . . 
COPY ./requirements.txt ./requirements.txt
EXPOSE 8000:8000
RUN pip3 install -r requirements.txt
CMD ["python3", "server.py"]

