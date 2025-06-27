# Assignment

# Chat Session Management System

A full-stack solution for managing chat sessions between customers and support agents, featuring a robust backend API and modern frontend interface.

## Features

- ✅ **Session Creation**: Start new chat sessions with one click
- 🔄 **Real-time Polling**: Check session status every second
- 🧑‍💻 **Agent Assignment**: Connect to available agents automatically
- ⏱️ **Session Monitoring**: Track session activity and timeouts
- 📊 **Status Tracking**: Visual feedback for all session states

## Technologies Used

### Backend
- ASP.NET Core Web API
- RabbitMQ for message queuing
- In-memory data storage (for demo purposes)

### Frontend
- Modern HTML5 & CSS3
- Vanilla JavaScript (no frameworks)
- Responsive design
- Clean, user-friendly interface

## Getting Started

### Prerequisites
- .NET 6 SDK
- RabbitMQ server (running locally)
- Modern web browser

## Usage

1. **Create a new session**
   - Click "Create Session" to initiate a new chat
   - The system will automatically assign a session ID

2. **Poll for status**
   - Session ID will appear in the input field
   - Click "Poll Session" to check current status
   - System updates every second automatically

3. **Session status indicators**
   - 🟢 `assigned`: Connected to an agent
   - 🟠 `pending`: Waiting in queue
   - 🔴 `error`: Something went wrong
   - ⚪ `inactive`: Session timed out


## API Endpoints

| Endpoint | Method | Description | Sample Response |
|----------|--------|-------------|-----------------|
| `/api/Chat/CreateSession` | POST | Create new chat session | `{ status: "available", sessionId: "guid" }` |
| `/api/Chat/Poll` | POST | Check session status | `{ status: "assigned", agent: "John" }` |



