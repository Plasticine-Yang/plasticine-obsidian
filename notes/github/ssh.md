# 开启 github 端口

```shell
Host github.com
  AddKeysToAgent yes
  IdentityFile ~/.ssh/github_ssh_private_key
  UseKeychain yes
```

验证是否生效

```shell
ssh -T git@github.com
```

# 启用私钥
```shell
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

# windows copy 文件到 linux 虚拟机后 ssh-add 报错
```shell
dos2unix ~/.ssh/id_ed25519
vim --clean ~/.ssh/id_ed25519
```

`:wq` 保存退出再试即可