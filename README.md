dot_files
===

我的zsh + vim + tmux 等等等的環境設定

![Imgur](http://i.imgur.com/5mM1HNb.png)

## Prerequirement

* zsh
* vim (with Python support)
* patch 過的字型（沒patch過的沒有powerline使用的特殊符號）
* python module: psutil (pip install psutil)

#### Installation

1. 把repository clone回去

         git clone git@github.com:alexw867/dot_files.git

2. 執行 install-env.sh ,會把該拉回來的都拉回來

        cd dot_files
        ./install-env.sh
        
3. 執行modules/powerline/setup.py

        cd modules/powerline
        sudo ./setup.py install
    
4. 重新登入

5. 執行vim，在vim內執行

        : PluginInstall
        
# 常見問題

* 如果vi出錯AttributeError: 'VimPowerline' object has no attribute 'setup'

    砍了 pip 的 powerline
    
        sudo pip uninstall powerline

* 沒有右側時間列
 檢查一下 /usr/local/bin/powerline 是否為 

     __ requires __ = 'powerline == beta'

 是的話整個檔案砍了,(也不知道是哪來的)
 然後去 module/powerline

        git pull origin master

        git checkout develop

        sudo python setup.py install
