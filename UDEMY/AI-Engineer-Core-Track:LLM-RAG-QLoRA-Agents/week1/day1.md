# Running llm locally with ollama
- downloaded ollama through ollama.com
- type ollama in terminal to see whether it is working or not
- try ollama serve to check whether it is running in some port or not
- try ollama run <some open source model name> to install llm into local machine
 - eg: ollama run gemma3:270m 
- we can see all open source models in ollama.com
- NOTE: we need a lot of ram to run big llm models locally
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

# using paid llm model
- he is using paid chatgpt
- he got the API to call gpt models
- kept API key in env file 
- he is using .ipynb files. it's a jupyter notebook, this notebook contains both text and code
- to run the notebook he selected a python kernal
- he is using curser(vs code alternative)
- he provided the repo which has all the code
- he opened day1.ipynb notebook
- he imports all the required this first
- he loaded apikey into notebook
- he prepared a dictionary to send to llm model
- he called llm model with dictonary and api key
- code looks like 
    - ```
        openai = OpenAi()
        messages = [
            {role: "system": "content": "youre a helpful assistant"},
            {role: "user", "content": "hi"}
        ]
        response = openai.chat.completions.create(model="get-5-nano", messages=messages)
        response.choices[0].message.content
        ```
- the he has pre built utility which has input of url and returns the site content
- he sent that content to llm model and asked it summaize
- he just added entire site description in the content of the user object