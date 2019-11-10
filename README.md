## Usage

Here are some example snippets to help you get started creating a container.

### docker-compose

Compatible with docker-compose v3 schemas.

```
---
version: "3"
services:
  vector_sdk:
    image: brushknight/vector-sdk-docker
    container_name: vector.sdk
    volumes:
      - </path/to/configs-folder>:/app/config
      - <path/to/your-code>:/app/code
    restart: unless-stopped
```