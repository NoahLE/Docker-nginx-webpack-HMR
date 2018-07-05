# Sandbox application

This is a sandbox application which uses Vue, webpack4, Docker, and nginx to serve a simple webpage.

Hot module replacement will hopefully be working soon...

## Installation

Before starting, make sure you have the following installed:

- Node
- Yarn
- Docker

Add `127.0.0.1 local.sandbox.com` to your `/private/etc/hosts` file.

1. Install the packages with `yarn`
2. Build the project for Docker with `docker-compose -f docker-compose.yml4 up`

## Notes

The application works with hot module replacement if you go to `local.sandbox.com:3000` or `localhost:3000`.

If you go to `local.sandbox.com` or `localhost`, nginx does not correctly proxy_pass the data to the `webpack-dev-server` running on port 3000.