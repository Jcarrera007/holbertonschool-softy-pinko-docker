FROM ubuntu:latest

RUN apt-get update \
	&& apt-get upgrade -y \
	&& apt-get install -y python3 python3-pip \
	&& rm -f /usr/lib/python*/EXTERNALLY-MANAGED \
	&& pip3 install --no-cache-dir flask \
	&& apt-get clean \
	&& rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY api.py /app/api.py

EXPOSE 5252

CMD ["python3", "/app/api.py"]