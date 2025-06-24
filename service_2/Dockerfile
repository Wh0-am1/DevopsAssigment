FROM python:3.13-alpine
RUN apk add --no-cache curl
COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/
COPY . /app
WORKDIR /app
RUN uv sync --locked
EXPOSE 8002
CMD ["uv", "run", "app.py"]
