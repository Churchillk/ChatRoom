# Chat Application

Welcome to the Chat Application! This project includes a simple chat server and client system implemented in Python. It allows multiple clients to connect to a server, exchange messages, and includes features for managing client connections.

## Features

- **Multi-Client Support**: Handles multiple client connections simultaneously.
- **Message Broadcasting**: Broadcasts messages to all connected clients.
- **Client Management**: Supports kicking clients by username and handles unexpected disconnections.
- **Server Commands**: Provides commands for shutting down the server and managing clients.

## Getting Started

To use this chat application, you need to have Python installed and ensure that the necessary libraries are available.

### Prerequisites

- Python 3.x
- `colorama` library for colored terminal text

### Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/yourusername/chat-application.git
    cd chat-application
    ```

2. **Install requirements:**

    Make sure the `colorama` library is installed in your environment. If not, you can install it using pip:

    ```bash
    pip install colorama
    ```

### Usage

1. **Run the Server:**

    Open a terminal, navigate to the project directory, and start the server:

    ```bash
    python server.py
    ```

2. **Run the Client:**

    Open another terminal (or multiple terminals for multiple clients), navigate to the project directory, and start the client:

    ```bash
    python client.py
    ```

    You will be prompted to enter a username. Each client should use a unique username.

3. **Sending Messages:**

    - Clients can send messages that will be broadcasted to all other connected clients.
    - To disconnect, type `!Leave`.

4. **Kicking Clients:**

    - The server supports kicking clients by username. Enter `kick <username>` in the server terminal to remove a specific client from the chat.

### Code Overview

#### `server.py`
- **Purpose**: Manages client connections, broadcasts messages, and handles server commands.
- **Key Functions**:
  - `Broadcast(message)`: Sends a message to all connected clients.
  - `handle_clients(conn, addr)`: Manages communication with a single client.
  - `kick_client(username)`: Kicks a client by username.
  - `server_commands()`: Handles server commands like shutdown and kick.

#### `client.py`
- **Purpose**: Connects to the server, sends messages, and receives messages from the server.
- **Key Functions**:
  - `create_client_socket()`: Establishes a connection to the server.
  - `send_msg(msg)`: Sends a message to the server.
  - `receive_msg()`: Receives and prints messages from the server.

### Contributing

If you have suggestions or improvements, feel free to open an issue or submit a pull request. Contributions are welcome!

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Contact

For any inquiries, please reach out to [your-email@example.com](mailto:your-email@example.com).

