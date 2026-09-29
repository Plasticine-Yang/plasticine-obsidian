
和 dsh 结合使用时会有没带上 session 头导致无法请求的问题解决

1. 安装社区插件
```shell
dsh plugin --profile web add dsh-opencode-go-plus
```

> 安装时如果遇到 `pnpm approve-builds`，需要去 `~/.dsh/profiles/web/.plugin-manager` 目录里执行 `pnpm approve-builds`，其他目录执行不生效

2. dsh web 页面里的插件配置里使用即可