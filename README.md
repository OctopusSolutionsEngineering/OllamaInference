A Docker image based off the instructions at https://cloud.google.com/run/docs/tutorials/gpu-gemma-with-ollama.

# Running the image

```bash
docker run -p 8080:8080 ghcr.io/octopussolutionsengineering/ollamainference:latest
```

# Testing the container

```bash
curl -X POST http://localhost:8080/v1/chat/completions \
  -H "Content-Type: application/json" \
  -d '{
    "model": "gemma3:1b",
    "messages": [
      {
        "role": "user",
        "content": "What is the capital of France?"
      }
    ]
  }'
```
 