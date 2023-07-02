## AliDrive-auto-check-in
> 基于[ImYrS/aliyun-auto-signin](https://github.com/ImYrS/aliyun-auto-signin)的自动签到

## 食用指南
---

### 1.  将本项目复制到自己的仓库
![1](IMG/1.0.png)
---
### 2.  获取GP_TOKEN
访问：[https://github.com/settings/apps](https://github.com/settings/apps)
![2.0](IMG/2.0.png)
![2.1](IMG/2.1.png)
![2.2](IMG/2.2.png)
---
### 3.  获取REFRESH_TOKENS
登录阿里云盘网页端，按**F12**，进入**Console**(**控制台**)
粘贴代码：
`JSON.parse(localStorage.token).refresh_token;`
(不需要两端的单引号)
![3.0](IMG/3.0.png)
---
### 4.  获取PUSHPLUS_TOKEN
**非必要操作**，每次签到完成后进行微信推送
访问：[https://www.pushplus.plus/](https://www.pushplus.plus/)
![4.0](IMG/4.0.png)
![4.1](IMG/4.1.png)
---
### 5.  填写变量参数
回到自己的仓库
分次创建GP_TOKEN、REFRESH_TOKENS、PUSHPLUS_TOKEN，并填入获得的数据 
其中REFRESH_TOKENS可以填入多个值来实现多账户签到，只需要用英文逗号隔开
XXXXXXXXXXXX,XXXXXXXXXXXX
![5.0](IMG/5.0.png)
![5.1](IMG/5.1.png)
---
### 6.  运行测试
![6.0](IMG/6.0.png)
![6.1](IMG/6.1.png)
![6.2](IMG/6.2.png)
![6.3](IMG/6.3.png)
![6.4](IMG/6.4.png)
---
### 7.  修改运行时间
进入`.github/workflow/signin.yaml`
默认**北京时间凌晨01：30**，参数为`'30 17 * * *'`，30代表分钟，17代表小时
可修改为想要的时间减8小时，比如我想在北京时间19：30运行，需设置为`'30 11 * * *'`
![7.0](IMG/7.0.png)
![7.1](IMG/7.1.png)
---