# 第一步 安装

安装`Termux`，[点击这里安装](https://f-droid.org/repo/com.termux_117.apk)

# 第二步 安装

输入指令更新pkg包管理器:

```shell
pkg update
pkg upgrade
```

输入指令以安装`Ubuntu虚拟容器`:

```shell
pkg install wget openssl-tool proot -y && hash -r && wget https://raw.githubusercontent.com/EXALAB/AnLinux-Resources/master/Scripts/Installer/Ubuntu/ubuntu.sh && bash ubuntu.sh
```

> 时间较长，过程中有`Y/n`并且卡住的时候请输入`y`

进入`Ubuntu虚拟容器`:

```shell
./start-ubuntu.sh
```

# 第三步 安装

输入指令更新apt包管理器:

```shell
apt-get update
apt-get upgrade
```

输入指令安装`git`，`Python`，`pip3`，`nano`:

```shell
apt install git
apt install python
apt install python3-pip
apt install nano
```

# 第四步 安装

输入指令clone仓库:

```git
git clone https://github.com/xtaodada/PagerMaid-Modify.git pagermaid && cd pagermaid
```

---

输入指令安装软件包(`可选`):

### 图片处理:

```shell
apt-get install imagemagick -y
```

### 系统信息:

```shell
apt-get install software-properties-common  && add-apt-repository ppa:dawidd0811/neofetch && apt-get update && apt-get install neofetch
```

### 二维码处理:

```shell
apt-get install libzbar-dev -y
```

### 光学识别:

```shell
apt-get install tesseract-ocr tesseract-ocr-all -y
```

### 任务执行:

```shell
apt-get install redis-server -y
```

---

## 安装依赖:

```shell
pip3 install -r requirements.txt
```

## 修改配置:

```shell
cp config.gen.yml config.yml
nano config.yml
```

> 复制`api_id`和`api_hash`值，填入`api_key`和`api_hash`

## 运行:

```python
python3 -m pagermaid
```

> 首次会提示登陆账号
