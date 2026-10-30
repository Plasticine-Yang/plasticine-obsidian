```yaml
      ollama:
        apiKeyEnv: OLLAMA_API_KEY
        api: openai-responses
        baseURL: https://ollama.com/v1
        models:
          - id: deepseek-v4.1-flash:1017
            name: deepseek-v4.1-flash:1017
            contextWindow: 1048576
            maxTokens: 384000
            input:
              - text
              - image
            reasoningEfforts:
              low: low
              high: high
              max: max
```