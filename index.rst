.. introduction to programming with python documentation master file, created by
   sphinx-quickstart on Sat Jun  9 11:24:58 2012.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Pythonを用いたプログラミング入門
================================


発表する人
----------

Noriyuki Hosaka

@bgnori(twitter)

http://github.com/bgnori



コンピュータをより身近に
------------------------

なんらかの形で毎日使う。もはや体の一部

直接つかうのは「アプリ」

しかし「出来合い」がほとんど

自分だけのアプリは作るには？


コンピュータとお話
------------------

何かしてほしい → 意志を伝える。

犬に芸をさせるような感じ = 命令の集まり

相手に合わせる必要 → プログラミング言語

平易なもので始める → Python


なんでPython?(1)
----------------

なにもかも0から作るわけではない

出来合いの部品が大事

DIY、ホームセンターでの買物

スーパーのお惣菜 v. 生きた鶏


なんでPython?(2)
----------------

シンプルさ

どこでも動く

反応をすぐに得られる

onlineのshell
  http://shell.appspot.com/

print, 値
---------

数値, 文字列, 真理値, 画面に表示

>>> 1
1
>>> 'python'
'python'
>>> 1 <  2
True
>>> print 'hello, python!'
'hello, python!'


変数, 代入
----------

名前と値を結びつける

>>> x = 1
>>> y = 2
>>> print x
1
>>> print y
2
>>> x = x + 1
>>> print x
2


配列(list), index, slice
-------------------------

>>> x = [1, 2, 4]
>>> x[0]
1
>>> x[2]
4
>>> x[1:]
[2, 4]
>>> x[2] =  10
>>> x[2] 
10
>>> x
[1, 2, 10]

参照
----

x,yそのものがlistなのではなく、

listを差し示している。

>>> x = [1, 2, 3]
>>> y = x
>>> y[0] = 4
>>> x[0]
4

辞書(dict)
----------

key, value

>>> d = {'a':1, 'b':'B', 'c':'paxil'}
{'a':1, 'b':'B', 'c':'paxil'}
>>> d['b']
'B'
>>> d[2]   # key error.

dir, help : 「自己紹介」をさせる
--------------------------------

>>> d = {}
>>> dir(d)
['__class__', '__cmp__', '__contains__',
'__delattr__', '__delitem__', '__doc__',
'__eq__', '__format__', '__ge__', 
(略)
>>> help(d)



if, else
--------

indentと'block'

>>> if True:
...     print 'Yes'
...     print 'We'
...     print 'Can'
... else:
...     print 'F'


while
-----

条件を満たす間、繰り返す

>>> x=0
>>> while(x<3):
...     print x
...     x = x+1
0
1
2

関数
----

処理の再利用

「ほしいこと」と「実現方法」の分解
(抽象化)

>>> def inc(x):
...     return x+1
>>> inc(5)
6
>>> inc(8)
9


スコープ
--------

>>> a = 4
>>> def inc_a(x):
...     return x + a
>>> inc_a(3)
7
>>> def inc_f(b):
        def g(x)
...         return x + b
...     return g
>>> f = inc_f(3)
>>> f(6)
9

import, dir
-----------
出来合いの部品を使う

>>> import urllib
>>> help(urllib)

充実したドキュメント
http://www.python.jp/doc/release/

urllib
------

web上のデータを取得するための部品

>>> import urllib
>>> data = urllib.urlopen('http://python.org/').read()
>>> data[:400]

正規表現
--------

文字列を見つけるための部品


>>> import re
>>> s = re.find('python', data).start()
>>> e = re.find('python', data).end()

まとめ
------

動かすために命令を出す

命令の集まりを作り出すこと

出来合いの部品をうまく使う

「巨人の肩の上に立つ」

Q & A
-----

 

おわり
------

ありがとうございました!

