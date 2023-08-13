
# ReqMock JavaScript Library

`ReqMock` is a powerful JavaScript library that simplifies network interactions by providing utilities for making HTTP requests, managing WebSocket connections, and tracking download progress.

## Features

- **Strong Requests**: Easily make HTTP requests with customizable headers and payloads, ensuring your data is transmitted securely.

- **WebSocket Connections**: Establish WebSocket connections and send real-time messages, enabling interactive communication between clients and servers.

- **Download Progress Tracking**: Track download progress when downloading files, allowing you to display accurate progress information to users.

- **Upload Files**: Upload files via FormData, making it seamless to send user-generated content to the server.

- **Customizable Headers and Payloads**: Set custom headers and payloads for requests, tailoring the interactions to your specific needs.

## Installation

To use `ReqMock` in your project, you can include it in your HTML:

```html
<script src="NOT UPLOADED YET"></script>
```

## Usage

### Making HTTP Requests

The `sendRequest(url, method)` function allows you to make HTTP requests with ease. You can specify the URL and HTTP method (defaulting to 'GET') for the request. Additionally, you can set headers and payloads using `setHeaders()` and `setPayload()` functions.

```javascript
const reqMock = new ReqMock();

reqMock.setHeaders({ 'Content-Type': 'application/json' });
reqMock.setPayload({ key: 'value' });

reqMock.sendRequest('https://api.example.com/data', 'POST')
  .then(data => console.log('API Response:', data))
  .catch(error => console.error('API Error:', error));
```

### Establishing WebSocket Connections

Use the `connectWebSocket(url)` function to establish WebSocket connections. You can send messages over the WebSocket using `sendWebSocketMessage()`.

```javascript
const reqMock = new ReqMock();
const wsUrl = 'wss://websocket.example.com';

reqMock.connectWebSocket(wsUrl)
  .then(socket => {
    console.log('WebSocket Connection:', socket);
    reqMock.sendWebSocketMessage(wsUrl, 'Hello, WebSocket!');
  })
  .catch(error => console.error('WebSocket Error:', error));
```

### Downloading Files with Progress

The `downloadFileWithProgress(url, filename, progressCallback)` function enables downloading files while tracking download progress.

```javascript
const reqMock = new ReqMock();
const fileUrl = 'https://example.com/large-file.zip';

reqMock.downloadFileWithProgress(fileUrl, 'large-file.zip', (progress) => {
  console.log(`Download Progress: ${progress}`);
});
```

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

## License

This project is licensed under the MIT License
```
