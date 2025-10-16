# Steps to custom changes

1. git clone git@github.com:josefsj3m/wuzapi.git
2. cd wuzapi
3. git checkout -b feature/webhook-no-proxy-v1.0.3
4. do development
5. Local test
    1. go build -o wuzapi .
    ./wuzapi
4. git add .
5. git commit -m "Use direct HTTP client (no proxy) for webhooks"
6. git push origin feature/webhook-no-proxy-v1.0.3

# Build docker image

1. docker build -t your-user/wuzapi:custom .
2. docker tag your-user/wuzapi:custom ghcr.io/your-user/wuzapi:custom
2. docker push ghcr.io/your-user/wuzapi:custom

# Modified files
1. clients.go
2. helpers.go
3. main.go
4. wmaiu.go