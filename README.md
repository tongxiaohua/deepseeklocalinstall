# DeepSeek���ز��𼰴˽�е�֪ʶ��̳�

## ˵��

* �⼸�콨�˸�΢��Ⱥ�������˶�AIӦ�õ��������Ҵ��۽磬���ᶨ��AI�����ع�������ҵ���뷨��Ⱥ��Ŀǰ���������Ǳ��ز���DEEPSEEK���˽��֪ʶ�⣬������������̳�,΢��Ⱥ�ŷ����ĵ�ĩβ��

* ԭ���Ľ̷̳��ڡ�ԭLinux����̡̳�Ŀ¼��

* �˽̵̳Ĳ��𻷾���windows����1.bģ������ʾ�����ԶԵ������ü���������Ҫ�󣬻������������и��˵��ԡ������ǽ�������Լ�������ѡ������ģ�ͣ�1.5bģ��Լ�������ϡ�

* �������Կ�ѧ�������������򵥡�



## ���ز���װ ollama

��ַ��https://ollama.com/download/windows

![alt text](image.png)

windows�İ�װ���ܼ򵥣����سɹ���һ·ȷ�����ɡ�

��װ�ɹ��󣬿���������������:

```bash
ollama -v
```

�����汾�ż���װ�ɹ���

![alt text](4fb6e65399635126adb965f5733ad28.png)


�����д򿪷�����
��סWIN+R������CMD��ȷ��
![alt text](image-4.png)


## ���ز���װdocker-desktop

������ַ��https://www.docker.com/

����AMD64�汾

![alt text](image-2.png)

��������Ȼ��һ·ȷ������װ��ɺ�������п�ݷ�ʽ�������С�

![alt text](b8ee6ebc73c01929368947a141e58d5.png)

docker-desktop��װ���п��ܻ������ܶ����⣬�󲿷ֶ�����Ϊ�����˱�ǽ����Դ����ѧ���������������ƹ���
![alt text](6031c5575e617f350e38c8021adac93.png)

## ����deepseekģ��

����������
```bash
ollama pull deepseek-r1:1.5b
```
����ָ��������DEEPSEEK-R1 1.5Bģ�ͣ�������Լ���Ӳ������ѡ��
����ʹ�õ�DEEPSEEKģ���У�


* ollama run deepseek-r1:1.5b,

* ollama run deepseek-r1:8b

* ollama run deepseek-r1:32b

* ollama run deepseek-r1:70b

* ollama run deepseek-r1:671b

�����ǲ�ͬ�汾�� DeepSeek ģ���ڱ��ز���ʱ������Ҫ�󣬰��� CPU���ڴ桢Ӳ�̺��Կ��ľ������ã�
* DeepSeek-R1-1.5B
CPU����� 4 �ˣ��Ƽ� Intel/AMD ��˴�������
�ڴ棺8GB+
Ӳ�̣�3GB+��ģ���ļ�Լ 1.5-2GB��
�Կ����Ǳ��裨�� CPU �������� GPU ���ٿ�ѡ 4GB+ �Դ棨�� GTX 1650��
���ó���������Դ�豸��������ݮ�ɡ��ɿ�ʼǱ���Ƕ��ʽϵͳ���������豸��
* DeepSeek-R1-7B
CPU��8 �����ϣ��Ƽ��ִ���� CPU��
�ڴ棺16GB+
Ӳ�̣�8GB+��ģ���ļ�Լ 4-5GB��
�Կ����Ƽ� 8GB+ �Դ棨�� RTX 3070/4060��
���ó�������С����ҵ���ؿ������ԡ��еȸ��Ӷ� NLP ���������ı�ժҪ�����롢���������ֶԻ�ϵͳ��
*  DeepSeek-R1-8B
CPU��8 �����ϣ��Ƽ��ִ���� CPU��
�ڴ棺16GB+
Ӳ�̣�8GB+��ģ���ļ�Լ 4-5GB��
�Կ����Ƽ� 8GB+ �Դ棨�� RTX 3070/4060��
���ó���������߾��ȵ�������������������ɡ��߼�������
* DeepSeek-R1-14B
CPU��12 ������
�ڴ棺32GB+
Ӳ�̣�15GB+
�Կ���16GB+ �Դ棨�� RTX 4090 �� A5000��
���ó�������ҵ���������񡢳��ı���������ɡ�
* DeepSeek-R1-32B
CPU��16 �����ϣ��� AMD Ryzen 9 �� Intel i9��
�ڴ棺64GB+
Ӳ�̣�30GB+
�Կ���24GB+ �Դ棨�� A100 40GB ��˫�� RTX 3090��
���ó������߾���רҵ�������񡢶�ģ̬����Ԥ����
* DeepSeek-R1-70B
CPU��32 �����ϣ��������� CPU��
�ڴ棺128GB+
Ӳ�̣�70GB+
�Կ����࿨���У��� 2x A100 80GB �� 4x RTX 4090��
���ó��������л���/������ҵ���߸��Ӷ���������
* DeepSeek-R1-671B
CPU��64 �����ϣ���������Ⱥ��
�ڴ棺512GB+
Ӳ�̣�300GB+
�Կ�����ڵ�ֲ�ʽѵ������ 8x A100/H100��
���ó����������ģ AI �о���ͨ���˹����ܣ�AGI��̽����


���غ��������ĵȴ���ollama֧�ֶϵ�������������ʱ�ص��������ػ��о�ϲ��

![alt text](image-3.png)


## ����DEEPSEKKģ��


```bash
ollama run deepseek-r1:1.5b
```


����һ���Ѿ��������������н��б��ضԻ��ˡ�
![alt text](image-10.png)

ʵ�ʿ�1.5Bȷʵ������

![alt text](image-11.png)
## ����dify������docker��ȡ���л���

```bash
git clone https://github.com/langgenius/dify.git
cd dify/docker
cp .env.example .env
docker compose up -d
```

github��Ҫ��ѧ���������� û��git��ͬѧ����ֱ������zip��ѹ���ҷ���һ�ݷ������̣�
����: https://pan.baidu.com/s/1cN7_LmdT0u-ZbANi0wmNTw?pwd=g5dn ��ȡ��: g5dn ����������ݺ�򿪰ٶ������ֻ�App������������Ŷ��
��ѹ��ע��·������dify-main������dify

��ȡdocker���������deepseekģ�Ϳ���ͬʱ����
![alt text](image-5.png)

![alt text](image-6.png)

������򿪣�http://localhost/install�����ĵȴ���
![alt text](image-7.png)


![alt text](image-8.png)��
�Լ�ע���˻�

![alt text](image-9.png)

ע������¼

## ����DEEPSEEK����ģ�͡�
![alt text](2556004308ae7d705e84742fe7f8d23.png)

![alt text](034656f0d4d71eaf3279191056972ea.png)

ע��ѡ��ollama����Ҫѡ��deepseek���������ߵ�ģ�ͣ���Ҫ���ѣ�ĿǰDEEPSEEK��ʱ�ر��˸��ѡ�

ollma�״ι������ܻᱨ��

![alt text](3d555608651d5274c002e757c4d58bd.png)

������ΪDOCKER������������絼�µģ����ñ��ػ���������
![alt text](33a8aa504e3daec787c9114bc755114.png)

![alt text](8ec71be5c72f4bc0acdec5fc4f2c955.png)

������ַ�ǣ�
```bash
http://host.docker.internal:11434
```

�����ɹ���
![alt text](image-12.png)

���Կ�ʼ����ҳ������

## ��������֪ʶ��
![alt text](0c7f078f0fbf17f43a0f65a9e000bb8.png)
![alt text](2dd28ed05ece70dcfdad106805a323c.png)

![alt text](46e105734ee36a0cd5dc1884d49a3f8.png)


## �½�Ӧ�ò�����֪ʶ��

![alt text](de9e7e86fe586f5cff0d64840f41342.png)
![alt text](95c9546869c2b599b95a52574e116d1.png)
![alt text](image-15.png)
![alt text](image-16.png)
![alt text](image-17.png)
![alt text](image-18.png)

��ʼ����ҳ�������ˣ����Կ���1.5B�������ϣ����ĵ������Ҳ����û��
![alt text](image-14.png)
![alt text](image-19.png)



## AIӦ�ý���Ⱥ

AIʱ��������һ��̽��ʵ����ص�Ӧ�ã�Ⱥ�������ѳ���200�ˣ�ֻ��ͨ��������룬

��ά����ڿ�����Ӻ�����Ⱥ��
![alt text](8ba2d055dff120cb4f12dbcb49bd30e.jpg)

