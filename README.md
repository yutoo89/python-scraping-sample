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
