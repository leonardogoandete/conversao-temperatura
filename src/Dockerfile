FROM ubuntu:22.04
RUN useradd app
RUN apt update && \
    apt install curl -y&& \
    curl -fsSL https://deb.nodesource.com/setup_20.x | bash && \
    apt-get install -y nodejs
WORKDIR /app
COPY . .
RUN npm install
EXPOSE 8080
ENTRYPOINT [ "node", "server.js" ]
USER app
