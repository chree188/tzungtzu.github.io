

### 准备 virtual environment 与 pyTelegramBotAPI

1. 命令行方式
    
    见  venv

2. IDE 方式
    使用 IDE 相比来说很方便。我们只需要新建一个项目，File - Settings - Project interpreter, 右侧的齿轮里即可选择 create VirtualEnv

    我建议将 VirtualEnv 选择到工程目录下，这样方便我们判断哪个 VirtualEnv 对应哪个项目。当然，如果你打算把代码 push 到 GitHub，记得把这个目录加到.gitignore里。

    之后我们点击加号，安装pyTelegramBotAPI这个 package，PyCharm 就会自动为我们安装好这个包了

### 我该怎么处理我的 TOKEN

### 项目结构


我们还需要导出依赖，方便别人也能够用啊！

很简单，进入到 virtual env，运行如下命令：

pip freeze > requirements.txt

别人用的时候，pip install -r requirements.txt就可以安装对应的依赖啦。


### webhook


### References:
1. [[Telegram bot 系列]0：用 Python 写一个 Telegram Bot 简单的回话 bot | 土豆不好吃](https://www.bennythink.com/tgbot0.html)