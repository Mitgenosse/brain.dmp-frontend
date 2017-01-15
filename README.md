# brain.dmp-frontend
Frontend for brain.dmp platform.

brain.dmp is a knowledge distribution/notepad platform. This frontend 
is fundamentally based on node.js and the React view library.

This brain.dmp frontend will be developed backend agnostic. It 
communicates with the backend via HTTP REST calls. 

## Documentation

The folder **docs/** contains several specification files.


## Run it

#### Development

```
npm start
```
Runs the node express server.js and webpack-dev-server. **_For development, use localhost:4711_**.

```
npm test
```
Runs mocha tests found in test/

#### Dist

```
npm run dist
```
Webpacks the src code and copies the server.js to dist dir.

Then start server.js, it will listen on port 4712 (by default).
server.js requires *express* and *request*.

## Environment variables

There are two nodejs express servers in this project: *server.js* and *server-backend.js*.
They can be run using several environment variables.

### server.js
Command | Purpose | Default
--- | --- | ---
APIBASEURI | The uri of the REST web api service to talk to. | http://localhost:4713 (server-backend.js backend mock)
PORT | The port to run on. | 4712

### server-backend.js

Command | Purpose | Default
--- | --- | ---
BACKEND_PORT | The port to run on. | 4713
