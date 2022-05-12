# my_link_hub

测试gitee互通

## 操作

1. 首先在github上面和gitee上面都需要同时绑定sshkey
2. 然后需要在github上面建立一个仓库
3. 在gitee上创建一个相同名称的仓库的时候 需要通过http链接将github仓库导入到gitee
4. 此时需要在当前项目.git/config中修改内容如下
  
> 代码展示

```js
`
    [core]
        repositoryformatversion = 0
        filemode = true
        bare = false
        logallrefupdates = true
        ignorecase = true
        precomposeunicode = true
    [remote "origin"]
            url = git@github.com:chrisworkalx/my_link_hub.git
            url = git@gitee.com:chrisworkalx/my_link_hub.git
            fetch = +refs/heads/*:refs/remotes/origin/*
    [branch "main"]
            remote = origin
            merge = refs/heads/main
            `
```

![](/imgs/操作1.png)