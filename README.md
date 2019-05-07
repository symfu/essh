# essh

ssh 登陆管理工具

![usage](./assets/essh.gif)

### 安装

```
go get -u github.com/seamounts/essh
```

### 配置

example:

```yaml
- name: 北京区
  user: root
  host: 1.2.3.4
  port: 22
  keypath: path-key

- name: 上海区
  user: root
  host: 5.6.7.8
  port: 22
  password: 123456

- name: 登陆后，执行shell命令
  user: root
  host: 10.2.3.4
  port: 22
  cmds:
    - cmd: ssh root@2.3.4.5

- name: 跳板机
  user: root
  host: 10.10.101.1
  port: 22
  jump:
    - user: root
      host: 10.10.101.2
      port: 22
```
