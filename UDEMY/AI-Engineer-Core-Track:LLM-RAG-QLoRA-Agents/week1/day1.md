# Running llm locally with ollama
- downloaded ollama through ollama.com
- type ollama in terminal to see whether it is working or not
- try ollama serve to check whether it is running in some port or not
- try ollama run <some open source model name> to install llm into local machine
 - eg: ollama run gemma3:270m 
- we can see all open source models in ollama.com
- check below block how it went in local
```
shiva@Shivas-MacBook-Air Ollama.app % ollama serve
Error: listen tcp 127.0.0.1:11434: bind: address already in use
shiva@Shivas-MacBook-Air Ollama.app % ollama run gemma3:270m
pulling manifest 
pulling 735af2139dc6: 100% ▕██████████████████▏ 291 MB                         
verifying sha256 digest 
writing manifest 
success 
>>> hi
Hi there! How can I help you today?


>>> s is m
That's a great question! 😊

>>> next
That's a very good and concise way to say it! 
```

# 