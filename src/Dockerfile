FROM ubuntu:22.04
RUN useradd app
ARG NODE_MAJOR=20
RUN apt update && \
    apt install curl -y&& \
    curl -fsSL https://deb.nodesource.com/setup_${NODE_MAJOR}.x | bash && \
    apt-get install -y nodejs
WORKDIR /app
COPY . .
RUN npm install
EXPOSE 8080
ENTRYPOINT [ "node", "server.js" ]
USER app
