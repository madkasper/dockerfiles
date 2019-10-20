FROM python:alpine3.7

COPY /www /cors-poc
WORKDIR /cors-poc/www
EXPOSE 8000

ENTRYPOINT [ "python3", "-m", "http.server", "8000", "--cgi" ]

