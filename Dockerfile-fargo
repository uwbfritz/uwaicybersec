FROM maven:3.8.4-openjdk-11-slim AS build
RUN apt-get update && apt-get install -y git nodejs npm && rm -rf /var/lib/apt/lists/*
WORKDIR /app
RUN git clone https://github.com/Intelligent-System-Lab/aicybersecurityedu.git . && \
    npm install && \
    mvn package
CMD [ "mvn", "spring-boot:run"]
