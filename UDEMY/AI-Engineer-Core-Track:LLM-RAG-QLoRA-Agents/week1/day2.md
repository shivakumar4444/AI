- closed source frontier models (Open AI GPT, Claude, Gemini, Grok etc,.)
- open source models (Llama from meta, mixtral from mistral, qwen from alibaba, gemma from google, phi from microsoft, deepseek fromm deepseek ai etc)
- 3 ways to use model
    - chat interface
    - cloud api
    - downlaod model locally and run
- in day2.ipynb he just imported all, get apikey, call llm model through api with headers and paylod
- code looks like
    - ``` 
        //imported api key inro api_key
        headers = {Authorization: f"Bearer {api_key}", "Content-Type": "application/json"}
        payload = {
            model: "model-name",
            messages: [
                {role: "system": "content": "youre a helpful assistant"},
                {role: "user", "content": "hi"}
            ]
        }
        response = requests.post(
            "https://api.openai.com/v1/chat/completions",
            headers= headers,
            json=payload
        )
        response.json()
        ``` 
- with the same code he runs gemini model by getting gemini api key and by changing model name in the code

#### hitting local models
- he already has ollama installed and some models downloaded
- now the code looks like
    - ``` 
        ollama_url = "http://localhost:5776/v1"
        ollama = OpenAI(base_url=ollama_url, api_key="icufi") // apikey can be anything as it is local model
        ``` 
- remaining all code same
- we just need to focus on model name api key and url to hit any model(locally, cloud)