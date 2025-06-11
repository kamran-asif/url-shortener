# URL Shortener Service

A simple URL shortener service written in Go that provides a REST API to create short URLs and redirect to original URLs.

## Features

- Create short URLs from long URLs
- Redirect to original URLs using short URLs
- Simple and fast MD5-based URL shortening
- RESTful API endpoints

## API Endpoints

- `GET /` - Root endpoint, returns "Hello World!"
- `POST /shorten` - Create a short URL
  - Request body: `{"url": "https://example.com"}`
  - Response: `{"short_url": "abc123de"}`
- `GET /redirect/{id}` - Redirect to original URL using short URL ID

## Running the Service

1. Make sure you have Go installed
2. Clone the repository
3. Run the server:
```bash
go run main.go
```
The server will start on port 3000.

## Example Usage

```bash
# Create a short URL
curl -X POST http://localhost:3000/shorten \
  -H "Content-Type: application/json" \
  -d '{"url": "https://example.com"}'

# Visit the short URL in your browser
# http://localhost:3000/redirect/{short_id}
``` 