```
docker run --rm -p 80:80 -v /workspaces/web-design-bem:/app python:3.9-slim python -m http.server -d /app 80
```