# 查看有哪些 session

```shell
playwright-cli list
```

# 打开 session

```shell
playwright-cli -s=foo-session open --headed \
  --profile="/path/to/profile" \
  https://example.com
```

默认是 `browserName: "chromium"` 和 `channel: "chrome"` 去打开，这时候会走系统 Chrome，如果想走 playwright 内置 Chrome，有两种方式：

## 1. 指定配置文件

```shell
cat > .local/config.json <<'JSON'
{
  "browser": {
    "browserName": "chromium",
    "launchOptions": {
      "executablePath": "/Users/foo/Library/Caches/ms-playwright/chromium-1232/chrome-mac-arm64/Google Chrome for Testing.app/Contents/MacOS/Google Chrome for Testing"
    }
  }
}
JSON

playwright-cli -s=foo-session open --headed \
  --config=.local/config.json \
  --profile="/path/to/profile" \
  https://example.com
```

## 2. 走默认配置

维护项目级 or 用户级的 `playwright-cli` 配置文件，指定走内置 Chrome

- 项目级：`.playwright/cli.config.json`
- 用户级：`~/.playwright/cli.config.json`

```json
{
  "browser": {
    "browserName": "chromium",
    "launchOptions": {
      "channel": "chromium"
    }
  }
}
```

 打开 session

```shell
playwright-cli -s=foo-session open --headed \
  --profile="/path/to/profile" \
  https://example.com
```

# 关闭 session

关闭指定 session

```shell
playwright-cli -s=foo-session close
```

关闭全部 session

```shell
playwright-cli close-all
```

强制关闭全部 session

```shell
playwright-cli kill-all
```