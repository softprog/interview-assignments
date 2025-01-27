## 短域名架构
### 需求概述
由于长域名对搜索引擎不友好，及不利于用户进行链接分享，故创建短域名服务，以实现将不定长得域名缩减到比较友好得长度。
### 短域名服务设计
#### 设计目标：
+ 对外提供短域名创建接口
+ 对外提供短域名转换长域名接口
#### 技术选型
+ 采用spring boot实现整体得api服务
+ 采用spring boot test进行单元测试
+ 采用jacoco进行覆盖率测试
+ 依赖包管理利用maven来进行处理
#### 设计思路
+ 首先需要对外提供2个接口
+ 需要一个短域名算法，支持短域名长度设置
+ 需要实现一个缓存结构，用于保存短域名和长域名的映射关系
+ 需要有缓存清理策略
#### 服务架构
![](https://github.com/softprog/interview-assignments/blob/master/java/%E6%9E%B6%E6%9E%84.png)
#### 代码实现测试情况
![](https://github.com/softprog/interview-assignments/blob/master/java/screenshot_20210803184642.png)
#### 服务假设
+ 缓存可配置，可清理
+ 接口支持可扩展，方便替换进程内缓存为分布式缓存
+ 接口支持filter进行安全性校验


