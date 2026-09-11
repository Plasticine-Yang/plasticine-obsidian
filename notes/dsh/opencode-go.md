# 解决无法使用

和 dsh 结合使用时会有没带上 session 头导致无法请求的问题解决

1. 安装社区插件
```shell
dsh plugin --profile web add dsh-opencode-session
```

# 使用 deepseek v4.1 flash

dsh 内置的 pi ai provider 配置里的 opencode-go 的模型 catalog 还没更新，无法选中 v4.1 flash 模型，按以下配置可启用成功：

```yaml
ui-onboarding:
  welcomeNoticeVersion: 2026-08-13.1
agent-presets:
  default: standard
permission:
  defaultPreset: danger-full-access
llm-pi-ai:
  providers:
    opencode-go:
      apiKeyEnv: OPENCODE_GO_API_KEY
      api: openai-completions
      baseURL: https://opencode.ai/zen/go/v1
      reasoning: max
      compat:
        thinkingFormat: deepseek
        supportsReasoningEffort: true
        requiresReasoningContentOnAssistantMessages: true
        supportsDeveloperRole: false
        supportsStore: false
        maxTokensField: max_tokens
      models:
        - id: deepseek-flash
          name: DeepSeek V4.1 Flash
          contextWindow: 1000000
          maxTokens: 256000
          input: [ text, image ]
          imagePixelBudget: 640000
          imageMaxBytes: 1048576
          reasoningEfforts:
            off:
            low: low
            high: high
            max: max
agent-default-model:
  provider: opencode-go
  model: deepseek-flash
  reasoningEffort: max
```