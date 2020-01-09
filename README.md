### 流程

1. 生成 ssh 部署公钥和私钥

```
ssh-keygen -t ed25519 -f .../.ssh/github-actions-deploy
```

2. 在 GitHub repo 的 `Settings/Deploy keys` 中添加刚刚生成的公钥
3. 在 GitHub repo 的 `Settings/Secrets` 中添加 `GH_ACTION_DEPLOY_KEY`，值为刚刚生成的私钥
4. 编写 git actions, 目录结构如下

```txt
.github
   └──workflows
        └──ci.yml
```

5. 在 package.json 配置 homepage: https://rectmoon.github.io/git-workflow-react-demo

6. 提交代码

7. 记得选择 gh-pages 发布的主题
