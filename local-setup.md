# Local Setup

1. Install Ollama

```
curl -fsSL https://ollama.com/install.sh | sh
OLLAMA_HOST=0.0.0.0:11434 ollama serve

or if not sharing on a network...
ollama serve
```

2. Install ZeroClaw

```
curl -fsSL https://raw.githubusercontent.com/zeroclaw-labs/zeroclaw/master/install.sh | bash
```

3. Get a model

```
ollama pull llama3.1:8b
ollama pull mistral:7b
ollama pull deepseek-coder:6.7b
ollama pull qwen3.5:9b
```

Remove
```
ollama list
ollama rm llama3:8b
```


4. Run the model and test

```
ollama run llama3.1:8b
hello
/bye
```

In a browser or curl

```
curl http://localhost:11434/api/tags
```

5. Setup ZeroClaw

```
nano ~/.bashrc
export PATH="/home/xxxxxx/.cargo/bin:$PATH"
zeroclaw onboard
```
