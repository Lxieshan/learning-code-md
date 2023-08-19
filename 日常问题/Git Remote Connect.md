# Git Remote Connect

## 1. ssh

## 1.1 本地生成 ssh

```bash
$ ssh-keygen -t rsa -C "your_email@example.com"
```

### 1.2 位置

```bash
.ssh/id_rsa
```

## 2. git init

- 进入待提交文件 
- 输入 `git init`
  - ![image-20230819181440871](/Users/xieshan/Library/Application Support/typora-user-images/image-20230819181440871.png)

## 3. git add .

- 使用 `git add .` 提交 
  - 注意 点 和 add 之间有空格
  - <img src="/Users/xieshan/Library/Application Support/typora-user-images/image-20230819181547354.png" alt="image-20230819181547354" style="zoom:50%;" />

## 4. git commit 

- git commit -m "描述文字"
  - ![image-20230819181703330](/Users/xieshan/Library/Application Support/typora-user-images/image-20230819181703330.png)

## 5. git remote add [origin] git@github.com : [L/repository]

- 添加远程连接
  - ![image-20230819181937693](/Users/xieshan/Library/Application Support/typora-user-images/image-20230819181937693.png)

## 5. git pull --rebase [origin] [master] 

- 本地和远程同步
  - <img src="/Users/xieshan/Library/Application Support/typora-user-images/image-20230819181813725.png" alt="image-20230819181813725" style="zoom:50%;" />

## 6. git push -u [origin] [master]

- 远程提交
  - ![image-20230819182045980](/Users/xieshan/Library/Application Support/typora-user-images/image-20230819182045980.png)

