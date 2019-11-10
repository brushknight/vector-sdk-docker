FROM python:3.6-buster

WORKDIR /app

COPY ./keep-alive.py /app/system/keep-alive.py

RUN apt-get update && apt-get install -y \
python3-pil.imagetk

RUN python3 -m pip install --user anki_vector

CMD python /app/system/keep-alive.py