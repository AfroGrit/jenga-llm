# Open-Source LLMs: Ollama 

### Running Ollama with Docker

```bash
docker run -it \
    --rm \
    -v ollama:/root/.ollama \
    -p 11434:11434 \
    --name ollama \
    ollama/ollama
```

### Smaller LLM - gemma:2b.

```bash
ollama pull gemma:2b
```

### Donwloading the weights

1. Instead of mapping the /root/.ollama folder to a named volume, let's map it to a local directory:

```bash
mkdir ollama_files

docker run -it \
    --rm \
    -v ./ollama_files:/root/.ollama \
    -p 11434:11434 \
    --name ollama \
    ollama/ollama
```
2. Pull the model

```bash
docker exec -it ollama ollama pull gemma:2b 
```

### Serving

1. build
```bash
docker build -t ollama-gemma2b .
```
2. run
```bash
docker run -it --rm -p 11434:11434 ollama-gemma2b
```

3. Let's test it with the following prompt:
```bash
prompt = "What's the formula for energy?"
```

Note: reproducibility 
```bash
response = client.chat.completions.create(
    #...
    temperature=0.0
)
```