```yaml
      command-code:
        apiKeyEnv: COMMAND_CODE_API_KEY
        api: openai-responses
        baseURL: https://api.commandcode.ai/provider/v1
        models:
          - id: deepseek/deepseek-v4.1-flash
            name: DeepSeek V4.1 Flash (latest)
            contextWindow: 1048576
            maxTokens: 384000
            input:
              - text
              - image
            reasoningEfforts:
              low: low
              high: high
              max: max
          - id: deepseek/deepseek-v4.1-flash-fast
            name: DeepSeek V4.1 Flash Fast (latest)
            contextWindow: 1048576
            maxTokens: 384000
            input:
              - text
              - image
            reasoningEfforts:
              low: low
              high: high
              max: max
          - id: z-ai/glm-5.3-flash
            name: GLM-5.3 Flash
            contextWindow: 1048576
            maxTokens: 384000
            input:
              - text
              - image
            reasoningEfforts:
              low: low
              high: high
              max: max
          - id: z-ai/glm-5.3-flashx
            name: GLM-5.3 FlashX
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