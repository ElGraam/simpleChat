# simpleChat

simpleChat is a simple UDP-based chat application implemented in Python. It consists of a server and client component, allowing multiple users to communicate in a chat room.

## Features

- UDP-based communication
- Multiple client support
- Username-based messaging
- Timeout mechanism for inactive clients

## Components

### Server (`server.py`)

The server component handles incoming messages and broadcasts them to all connected clients. Key features include:

- Listens on localhost:65432
- Manages connected clients
- Broadcasts messages to all active clients
- Implements a 60-second timeout for inactive clients

### Client (`client.py`)

The client component allows users to connect to the server and exchange messages. Key features include:

- Connects to the server at localhost:65432
- Supports sending and receiving messages
- Uses threading to handle simultaneous sending and receiving of messages

## Usage

1. Start the server:
   ```
   python server.py
   ```

2. Run the client(s):
   ```
   python client.py
   ```

3. When prompted, enter a username for each client.

4. Start chatting! Messages sent from one client will be broadcast to all connected clients.

## Requirements

- Python 3.x

