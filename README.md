# OpenChat

OpenChat is a simple real-time chat application built with Python and Flask.

The project uses Flask-SocketIO for real-time communication and SQLite to store messages. It was mainly made to experiment with WebSockets, server-side events and handling multiple users at the same time.

## Features

- Real-time messaging
- Message history stored in SQLite
- Connected user counter
- Basic VIP system
- Automatic loading of previous messages
- Simple web interface

## Technologies

- Python
- Flask
- Flask-SocketIO
- Flask-SQLAlchemy
- SQLite
- HTML / CSS / JavaScript

## Installation

Clone the repository:

```bash
git clone https://github.com/victorofsec/OpenChat.git
cd OpenChat
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Linux/macOS:

```bash
source venv/bin/activate
```

Or on Windows:

```powershell
venv\Scripts\activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

Then start the application:

```bash
python app.py
```

The application will be available at:

```text
http://127.0.0.1:5000
```

## How it works

Messages are sent through a WebSocket connection using Flask-SocketIO.

When a message is sent, it is saved in the SQLite database and broadcast to the other connected users. When someone joins the chat, the previous messages are loaded from the database.

The project is fairly small, so most of the backend logic is contained in `app.py`.

## Project structure

```text
OpenChat/
├── app.py
├── requirements.txt
├── start.sh
├── Procfile
├── templates/
├── static/
└── instance/
```

## Why I made it

I made OpenChat to learn more about real-time applications and how WebSockets work with a Python backend.

There are still things I would improve, especially the authentication and security side of the project.

## License

This project is for educational and personal use.
