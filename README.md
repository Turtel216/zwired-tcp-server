# TCP Server in Zig

This repository contains a configurable TCP server implemented in [Zig](https://ziglang.org/). The project is intended for educational purposes, showcasing how to build a simple, yet flexible, server using Zig's low-level networking capabilities.

## Features

- **Configurable Port and Address:** Easily customize the server's listening address and port.  
- **Concurrent Connections:** Accepts multiple client connections concurrently.  
- **Simple Protocol Handling:** Handles incoming client messages with basic request-response logic.  
- **Lightweight and Efficient:** Built with Zig's minimal runtime and efficient memory management.  

## Prerequisites

- Zig (version ≥ 0.12.0 recommended)  
- A working internet connection if you plan to test across networks  

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Turtel216/wired-tcp-server.git
cd wired-tcp-server
```

### 2. Build the Project

```bash
zig build
```

### 3. Run the Server

The server defaults to `localhost:8080`. You can override these defaults using command-line arguments.

```bash
zig-out/bin/tcp_server [host] [port]
```

**Examples:**

```bash
# Run with default settings (localhost:8080)
zig-out/bin/tcp_server

# Run on a custom port
zig-out/bin/tcp_server 127.0.0.1 9090
```

### 4. Test the Server

You can test the server using tools like `telnet` or `netcat`.

```bash
nc 127.0.0.1 8080
```

Then, type messages to interact with the server.

## Configuration

The server can be configured by editing the `config.zig` file or passing arguments at startup. Options include:

- `host`: The IP address to bind the server to (default: `127.0.0.1`).  
- `port`: The port number to listen on (default: `8080`).  
- `max_connections`: Maximum number of simultaneous clients (default: `10`).  

## Code Structure

```
.
├── src
│   ├── main.zig       # Entry point and server logic
│   ├── config.zig     # Configuration settings
│   └── utils.zig      # Utility functions
├── zig-out            # Compiled binaries
├── build.zig          # Zig build script
└── README.md          # Project documentation
```

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request if you'd like to improve the codebase or documentation.

## License

This project is licensed under the [MIT License](LICENSE).