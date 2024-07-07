

### Q1. Running Ollama with Docker
Let's run ollama with Docker. We will need to execute the same command as in the lectures:
What's the version of ollama client?

```bash
root@8ec2a87dfb35:/# ollama -v
ollama version is 0.1.48
```

### Q2. Downloading an LLM
What's the content of the file related to gemma?
```bash
root@8ec2a87dfb35:~/.ollama/models/manifests/registry.ollama.ai/library/gemma# ls -ali
total 12
1074303 drwxr-xr-x 2 root root 4096 Jul  7 19:08 .
1074302 drwxr-xr-x 3 root root 4096 Jul  7 19:08 ..
1074304 -rw-r--r-- 1 root root  856 Jul  7 19:08 2b
```

### Q3. Running the LLM
Test the following prompt: "10 * 10". What's the answer?
```bash
root@8ec2a87dfb35:~# ollama run gemma:2b
>>> "10 * 10"
Sure, here is the model you requested:
```
10 * 10
```
This model represents the mathematical operation 
of multiplying two 10s, which is 100.
```

### Q4. Donwloading the weights
What's the size of the ollama_files/models folder?
```bash
root@c2e4f1adbff3:~/.ollama# du -h 
8.0K    ./models/manifests/registry.ollama.ai/library/gemma
12K     ./models/manifests/registry.ollama.ai/library
16K     ./models/manifests/registry.ollama.ai
20K     ./models/manifests
1.6G    ./models/blobs
1.6G    ./models
1.6G    .
```

Q5. Adding the weights
