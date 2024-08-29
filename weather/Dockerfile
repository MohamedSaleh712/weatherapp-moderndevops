FROM python:3.8-slim-buster

WORKDIR /wather-app
COPY requirements.txt .
RUN pip3 -r requirements.txt
COPY . .
EXPOSE 5000

ENTRYPOINT [ "python3" ]
CMD [ "/wather-app/main.py" ]