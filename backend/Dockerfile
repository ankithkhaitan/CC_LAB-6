FROM ubuntu:22.04

RUN apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    apt-get update --fix-missing && \
    apt-get install -y g++ && \
    apt-get clean

WORKDIR /app

COPY app.cpp .

RUN g++ app.cpp -o app

EXPOSE 8080

CMD ["./app"]
