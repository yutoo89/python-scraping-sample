# selenium の install

## pip の install

```bash
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python3 get-pip.py
```

確認

```
which pip
/usr/local/bin/pip
```

パスを通す

```
code ~/.bash_profile
```

~/.bash_profile に追記

```
export PATH=$PATH:/usr/local/bin/pip
```

```
source ~/.bash_profile
pip -V
pip 22.1.2 from /usr/local/lib/python3.9/site-packages/pip (python 3.9)
```

## selenium の install

```bash
pip install selenium
```

selenuim 以外にもスクレイピングのツールはあるが、ブラウザの操作には selenium が適している。

BeautifulSoup や Scrapy はデータ取得がメインのときに使う。

## Chrome ドライバーの install

selenium には web ドライバが付属していない。
ブラウザを操作するためには web ドライバが必要。

```bash
brew install chromedriver
```

# Jupyter Notebook install

## python ライブラリ install

```bash
pip install \
    pandas \
    matplotlib \
    seaborn \
    numpy \
    scipy \
    ipython \
    scikit-learn \
    mglearn \
    jupyterlab \
    graphviz \
    tabulate \
    notebook \
    jupyter-contrib-nbextensions \
    jupyter-nbextensions-configurator
```

Jupyter 起動

```bash
jupyter notebook --allow-root --ip=0.0.0.0
```

# selenium 起動

```py
from selenium import webdriver
browser = webdriver.Chrome()
```

上記を実行すればブラウザが起動する。
初回は chromedriver の開発元が未確認のため開けないと表示される。
その場合、システム環境設定 > セキュリティとプライバシー > 一般タブで許可する。
