# Networking 101
## Sockets and the Life of a Packet

## Pre-requisites:
To follow along and do the exercises in the workshop, you should download:
- Rancher Desktop via Self-Service
- Wireshark

# Useful commands for the workshop

## Docker

```sh
docker-compose down
docker-compose up --build -d
docker exec -it server bash
```

## strace

### Server

```sh
strace -e trace=network nc -l -p $PORT # Start netcat in listening mode and use strace to trace only networking-related system calls (like socket, bind, accept, connect, etc.)
```

### Client
```sh
echo "Hello from client" | nc localhost 12345
```
