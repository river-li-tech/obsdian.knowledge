**github添加sshkey**
- 生成 SSH key

```bash
ssh-keygen -t ed25519 -C "你的GitHub邮箱"
```

- 启动 agent 并加入 key

```bash
eval "$(ssh-agent -s)"
ssh-add --apple-use-keychain ~/.ssh/id_ed25519
```

- 复制公钥

```bash
pbcopy < ~/.ssh/id_ed25519.pub
```

- 测试 SSH 是否通

```bash
ssh -T git@github.com
```

