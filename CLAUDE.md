# FastAPI Gateway 

Create a configuration for the FastAPI Gateway 

Require a working example with the Admin screen enable. 
User should be able to login and review Admin screen 

Ensure Configuration include Simulated SSO

Include Authentication Token 

Gateway should be able to redirect Calls to Two Different LLMs

Also include a RAG Service 

I just need a minimal configuration that includes the Admin UI 

```
model_list:
  - model_name: ollama-llama3.2 
    litellm_params: # all params accepted by litellm.completion() - https://docs.litellm.ai/docs/completion/input
      model: ollama-llama3.2:latest  ### MODEL NAME sent to `litellm.completion()` ###
      api_base: OLLAMA_BASE_URL=http://localhost:11434
      api_key: "NO_KEY" # does os.getenv("AZURE_API_KEY_EU")
      rpm: 6      # [OPTIONAL] Rate limit for this deployment: in requests per minute (rpm)
  - model_name: anthropic
    litellm_params:
      model: anthropic/claude-sonnet-4-6
 ```
