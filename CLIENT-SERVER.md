When you view a webpage in your browser, you are making a request to another computer on the internet, which then provides you the webpage as a response. That computer you are talking to via the internet is a web server. A web server receives HTTP requests from a client, like your browser, and provides an HTTP response, like an HTML page or JSON from an API
Creating a Basic HTTP Server
mkdir first-servers
cd first-servers
touch hello.js
nano hello.js
first-servers/hello.js
const http = require("http");
first-servers/hello.js
const host = 'localhost';
const port = 8000;
first-servers/hello.js
const requestListener = function (req, res) {
    res.writeHead(200);
    res.end("My first server!");
};

const server = http.createServer(requestListener);
server.listen(port, host, () => {
    console.log(`Server is running on http://${host}:${port}`);
});

node hello.js
Server is running on http://localhost:8000
My first server!




