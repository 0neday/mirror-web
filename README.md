# NJCIT mirrors ��ҳ

## ���� Demo

### ֱ�ӱ���

��վʹ�� Jekyll ��д����ʹ�� babel ���� ECMAScript6����˱��밲װ ruby >= 2.0 �� nodejs.

### For Centos
1.��װ nodejs
```
yum install nodejs
```
2.��װ ruby 2.2.4 and rubygems

Step 1: Install Required Packages
```
yum install gcc-c++ patch readline readline-devel zlib zlib-devel
yum install libyaml-devel libffi-devel openssl-devel make
yum install bzip2 autoconf automake libtool bison iconv-devel sqlite-devel
```
Step 2: Compile ruby 2.2.4 source code
```
wget -c https://cache.ruby-lang.org/pub/ruby/2.2/ruby-2.2.4.tar.gz
```
Step 3: Install rubygems
```
wget -c https://rubygems.org/rubygems/rubygems-2.4.8.tgz
ruby setup.rb
```
3. ��װ bundle �� build
```
gem install bundle
gem install build
```
4. Fork mirrors source code

```
bundle install
jekyll build
```

### Build In Docker
```
cd mirror-web
docker build -t builden -f Dockerfile.build .
docker run -it -v /path/to/mirror-web/:/data builden
```

Ϊ�������У�һЩ��̬�����ļ���Ҫ����

```
wget https://mirrors.njcit.cn/static/tunasync.json -O static/tunasync.json
wget https://mirrors.njcit.cn/static/tunet.json -O static/tunet.json
mkdir -p static/status
wget https://mirrors.njcit.cn/static/status/isoinfo.json -O static/status/isoinfo.json
```

֮�� `jekyll serve` �������� demo.

## �����ĵ�

### ��������

1. Fork ����Ŀ�� clone
2. ������֧ `git checkout -b foo-doc`
3. �� `_posts/help` �н����ĵ��ļ����ļ�����ʽΪ `��-��-��-����.md`
4. �� markdown �﷨��д�ĵ�
5. �ύ�����ʹ���
6. ���� Pull Request

### д���淶

1. ������Բ�֪���ľ�����Ŀ��������һ���仰���ܸ���Ŀ
2. д��ʹ�÷���, ʹ�� Github Flavored Markdown ��ʽ
3. ��Ӣ���ַ���Ӧ��һ���ո�

### �����÷�

#### ��ѡ��
���� <http://mirrors.njcit.cn/help/tensorflow/> �У�ͨ����ѡ�����ϵͳ�Ͱ汾�ţ�����ֱ��ʹ�� Vue.js
