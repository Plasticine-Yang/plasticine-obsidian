# 启动

```shell
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --remote-debugging-address=127.0.0.1 \
  --remote-debugging-port=9222 \
  --remote-allow-origins="*" \
  --user-data-dir="$HOME/chrome-cdp-profile"
```
  
# 验证

```shell
curl http://127.0.0.1:9222/json/version
curl http://127.0.0.1:9222/json/list
```

## 正常打开 chrome

```shell
open -na "Google Chrome"
```