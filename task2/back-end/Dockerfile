FROM ubuntu:latest

WORKDIR /app

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y python3 python3-pip && \
    rm -f /usr/lib/python*/EXTERNALLY-MANAGED

RUN pip3 install flask

COPY ./api.py /app/api.py

EXPOSE 5252

CMD ["python3", "api.py"]
