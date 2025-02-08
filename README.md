# DeepSeek本地部署及搭建私有的知识库教程

## 说明

* 这几天建了个微信群，多数人对AI应用的讨论让我大开眼界，更坚定了AI可以重构所有行业的想法，群里目前需求最多的是本地部署DEEPSEEK并搭建私有知识库，所以做了这个教程,微信群号放在文档末尾。

* 原来的教程放在《原Linux部署教程》目录下

* 此教程的部署环境是windows，用1.b模型做演示，所以对电脑配置几乎无配置要求，基本适用于所有个人电脑。但还是建议根据自己的配置选择更大的模型，1.5b模型约等于智障。

* 如果你可以科学上网，步骤会更简单。



## 下载并安装 ollama

地址：https://ollama.com/download/windows

![alt text](image.png)

windows的安装包很简单，下载成功后，一路确定即可。

安装成功后，可以在命令行运行:

```bash
ollama -v
```

看到版本号即安装成功。

![alt text](4fb6e65399635126adb965f5733ad28.png)


命令行打开方法：
按住WIN+R，输入CMD，确定
![alt text](image-4.png)


## 下载并安装docker-desktop

官网地址：https://www.docker.com/

下载AMD64版本

![alt text](image-2.png)

下载完仍然是一路确定。安装完成后桌面会有快捷方式，打开运行。

![alt text](b8ee6ebc73c01929368947a141e58d5.png)

docker-desktop安装运行可能会遇到很多问题，大部分都是因为依赖了被墙的资源，科学上网基本都可以绕过。
![alt text](6031c5575e617f350e38c8021adac93.png)

## 下载deepseek模型

命令行运行
```bash
ollama pull deepseek-r1:1.5b
```
上述指令是运行DEEPSEEK-R1 1.5B模型，请根据自己的硬件性能选择
可以使用的DEEPSEEK模型有：


* ollama run deepseek-r1:1.5b,

* ollama run deepseek-r1:8b

* ollama run deepseek-r1:32b

* ollama run deepseek-r1:70b

* ollama run deepseek-r1:671b

以下是不同版本的 DeepSeek 模型在本地部署时的性能要求，包括 CPU、内存、硬盘和显卡的具体配置：
* DeepSeek-R1-1.5B
CPU：最低 4 核（推荐 Intel/AMD 多核处理器）
内存：8GB+
硬盘：3GB+（模型文件约 1.5-2GB）
显卡：非必需（纯 CPU 推理），若 GPU 加速可选 4GB+ 显存（如 GTX 1650）
适用场景：低资源设备部署，如树莓派、旧款笔记本、嵌入式系统或物联网设备。
* DeepSeek-R1-7B
CPU：8 核以上（推荐现代多核 CPU）
内存：16GB+
硬盘：8GB+（模型文件约 4-5GB）
显卡：推荐 8GB+ 显存（如 RTX 3070/4060）
适用场景：中小型企业本地开发测试、中等复杂度 NLP 任务，例如文本摘要、翻译、轻量级多轮对话系统。
*  DeepSeek-R1-8B
CPU：8 核以上（推荐现代多核 CPU）
内存：16GB+
硬盘：8GB+（模型文件约 4-5GB）
显卡：推荐 8GB+ 显存（如 RTX 3070/4060）
适用场景：需更高精度的轻量级任务（如代码生成、逻辑推理）。
* DeepSeek-R1-14B
CPU：12 核以上
内存：32GB+
硬盘：15GB+
显卡：16GB+ 显存（如 RTX 4090 或 A5000）
适用场景：企业级复杂任务、长文本理解与生成。
* DeepSeek-R1-32B
CPU：16 核以上（如 AMD Ryzen 9 或 Intel i9）
内存：64GB+
硬盘：30GB+
显卡：24GB+ 显存（如 A100 40GB 或双卡 RTX 3090）
适用场景：高精度专业领域任务、多模态任务预处理。
* DeepSeek-R1-70B
CPU：32 核以上（服务器级 CPU）
内存：128GB+
硬盘：70GB+
显卡：多卡并行（如 2x A100 80GB 或 4x RTX 4090）
适用场景：科研机构/大型企业、高复杂度生成任务。
* DeepSeek-R1-671B
CPU：64 核以上（服务器集群）
内存：512GB+
硬盘：300GB+
显卡：多节点分布式训练（如 8x A100/H100）
适用场景：超大规模 AI 研究、通用人工智能（AGI）探索。


下载很慢，耐心等待，ollama支持断点续传，下载慢时关掉重新下载会有惊喜。

![alt text](image-3.png)


## 运行DEEPSEKK模型


```bash
ollama run deepseek-r1:1.5b
```


到这一步已经可以在命令行中进行本地对话了。
![alt text](image-10.png)

实际看1.5B确实是智障

![alt text](image-11.png)
## 下载dify，并用docker获取运行环境

```bash
git clone https://github.com/langgenius/dify.git
cd dify/docker
cp .env.example .env
docker compose up -d
```

github需要科学上网，本地 没有git的同学可以直接下载zip解压，我放了一份放在网盘：
链接: https://pan.baidu.com/s/1cN7_LmdT0u-ZbANi0wmNTw?pwd=g5dn 提取码: g5dn 复制这段内容后打开百度网盘手机App，操作更方便哦。
解压后注意路径，是dify-main，不是dify

拉取docker镜像和下载deepseek模型可以同时进行
![alt text](image-5.png)

![alt text](image-6.png)

浏览器打开：http://localhost/install，耐心等待。
![alt text](image-7.png)


![alt text](image-8.png)，
自己注册账户

![alt text](image-9.png)

注册完后登录

## 关联DEEPSEEK本地模型。
![alt text](2556004308ae7d705e84742fe7f8d23.png)

![alt text](034656f0d4d71eaf3279191056972ea.png)

注意选择ollama，不要选择deepseek，那是在线的模型，需要付费，目前DEEPSEEK暂时关闭了付费。

ollma首次关联可能会报错。

![alt text](3d555608651d5274c002e757c4d58bd.png)

这是因为DOCKER与物理机的网络导致的，配置本地环境变量：
![alt text](33a8aa504e3daec787c9114bc755114.png)

![alt text](8ec71be5c72f4bc0acdec5fc4f2c955.png)

关联地址是：
```bash
http://host.docker.internal:11434
```

关联成功后：
![alt text](image-12.png)

可以开始用网页聊天了

## 创建本地知识库
![alt text](0c7f078f0fbf17f43a0f65a9e000bb8.png)
![alt text](2dd28ed05ece70dcfdad106805a323c.png)

![alt text](46e105734ee36a0cd5dc1884d49a3f8.png)


## 新建应用并关联知识库

![alt text](de9e7e86fe586f5cff0d64840f41342.png)
![alt text](95c9546869c2b599b95a52574e116d1.png)
![alt text](image-15.png)
![alt text](image-16.png)
![alt text](image-17.png)
![alt text](image-18.png)

开始用网页版聊天了，可以看出1.5B就是智障，对文档的理解也基本没有
![alt text](image-14.png)
![alt text](image-19.png)



## AI应用交流群

AI时代，我们一起探讨实际落地的应用，群聊人数已超过200人，只能通过邀请加入，

二维码过期可以添加好友拉群：
![alt text](8ba2d055dff120cb4f12dbcb49bd30e.jpg)

