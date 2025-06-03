# WebSocket
A WebSocket is a communication protocol that provides full-duplex, bi-directional communication between a client (like your browser) and a server over a single, long-lived TCP connection. Unlike the traditional HTTP request-response model, WebSockets allow real-time communication with low latency.

<h1>🔍 Key Characteristics:</h1>
✅ Persistent Connection: Once the WebSocket connection is established, it stays open, allowing data to flow in both directions until one side closes it.<br>
✅ Low Overhead: After the initial handshake, data can be sent without the overhead of HTTP headers.<br>

✅ Real-Time Communication: Ideal for applications where you need instant updates (e.g., chat apps, online games, live sports scores).



<h1>Implementation:</h1>
This is a practice project demonstrating a simple WebSocket-based chat application using Node.js, Express, and Socket.IO. It’s not intended to be a full-fledged production app, but rather a learning exercise to understand how WebSockets work.

<h2>🚀 Features:</h2>
Real-time messaging using WebSocket (via Socket.IO) <br>
Broadcasts messages to all connected users <br>
Simple front-end with an input field and a send button

/public
  └── index.html        # Frontend HTML with Socket.IO client<br>

server.js              # Node.js + Express server with Socket.IO

<h2>🔌 How it Works:</h2>
The server sets up an Express app and integrates Socket.IO for real-time communication.<br>
When a user connects to the server, they can send a message using the input box.<br>
The message is sent to the server using socket.emit("message", message).<br>
The server listens for the "message" event and then broadcasts the message to all connected clients using io.emit("message", message).<br>
Every client receives the message and appends it to the DOM.

<h2>📦 Dependencies:</h2>
Express<br>
Socket.IO<br>
Node.js

