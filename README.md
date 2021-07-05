# flask

flask program

# flask

## 环境安装

### 安装 pip

```
curl https://bootstrap.pypa.io/get-pip.py | python3
```

配置路径

```
vi  ~/.bash_profile
export "PATH=/Users/guzhongyu/Library/Python/3.8/bin:$PATH"
source ~/.bash_profile
echo $PATH
```

### 创建虚拟环境

#### pipenv

```
pip --default-timeout=100 install pipenv -i http://pypi.douban.com/simple/ --trusted-host pypi.douban.com
```

设置镜像源地址

```
pipenv install --pypi-mirror https://pypi.doubanio.com/simple flask
```

如果想对项目全局（per-project）设置，可以修改 Pipfile 中 [[source]] 小节：

```
url = "https://pypi.doubanio.com/simple"
verify_ssl = true
name = "douban"
```

#### 项目下创建环境

```
pipenv install
```

显式激活虚拟环境

```
pipenv shell
```

退出虚拟环境

```
exit
```

不显式激活虚拟环境

```
pipenv run python hello.py
```

### 管理依赖、

使用 pipenv 安装自动维护 Pipfile 和 Pipfile.lock

```
pipenv install module
```

查看安装环境

```
pipenv graph
```

### 安装 flask

```
pipenv install flask
```

更新版本

```
pipenv update flask
```

## 启动最小 flask

hello.py

```
from flask import Flask
app=Flask(__name__)
@app.route('/')
def index():
    return 'Hello world!'
```

启动命令

```
pipenv shell
export FLASK_APP=hello.py
flask run
```
# server-file
