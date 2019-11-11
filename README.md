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
      - </path/to/configs-folder>:/root/.anki_vector/
      - <path/to/your-code>:/app/code
    restart: unless-stopped
```

## How to generate configs

If you already have config files, you can just provide those files via config folder. 
If you have not, just follow the list.

1. Run container with docker compose
2. Run `docker exec -it vector.sdk python -m anki_vector.configure`
3. Follow the setup wizard
4. Find `sdk_config.ini` and `Vector-XXXX-XXXXXXXX.cert` in </path/to/configs-folder>

