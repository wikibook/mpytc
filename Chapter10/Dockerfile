FROM python:3.8-slim

RUN apt-get -q update && apt-get -q install -y wget 

COPY ./server.py ./
COPY ./requirements.txt ./

RUN wget -q https://raw.githubusercontent.com/wikibook/mpytc/main/Chapter10/convnet.pth
RUN wget -q https://github.com/wikibook/mpytc/raw/main/Chapter10/digit_image.jpg

RUN pip install --no-cache-dir -r requirements.txt


USER root
ENTRYPOINT ["python", "server.py"]
