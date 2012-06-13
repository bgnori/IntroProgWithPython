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

onlineの実行環境
  http://www.compileonline.com/execute_python_online.php

値, print
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

>>> xs = [1, 2, 4]
>>> xs[0]
1
>>> xs[2]
4
>>> xs[1:]
[2, 4]
>>> xs[2] = 10 # GAE上では破壊的変更は出来ない
>>> xs[2] 
10
>>> xs
[1, 2, 10]

参照
----

x,yそのものがlistなのではなく、

listを差し示している。

>>> xs = [1, 2, 3]
>>> ys = xs
>>> ys[0] = 4 # GAE上では破壊的変更は出来ない
>>> xs[0]
4

辞書(dict)
----------

key, value

>>> d = {'a':1, 'b':'B', 3:'foo'}
{'a':1, 'b':'B', 3:'foo'}
>>> d['b']
'B'
>>> d[3]
'foo'
>>> d[2]   # key error.


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

関数(例をさらに)
----------------

>>> def times(s, n):
...     return s*n
>>> times('abc', 3)
'abcabcabc'
>>> def sum(x, y, z):
...     return x+y+z
>>> sum(1, 2, 3)
6
>>> def herasu(x): # 悪い名前
...     return x+1
>>> herasu(5)
6

スコープ
--------

>>> def foo(x):
...     y = x+3
...     return y*x
>>> foo(3)
18
>>> y # not defined.
>>> a = 4
>>> def inc_a(x):
...     return x + a
>>> inc_a(3)
7

object, help, dir
-----------------

>>> d = {}
>>> help(d)
>>> help(1)
>>> dir(d)
['__class__', '__cmp__', '__contains__',
'__delattr__', '__delitem__', '__doc__',
'__eq__', '__format__', '__ge__', 
(略)


関数自体もobject
----------------

>>> def inc_f(b):
        def g(x)
...         return x + b
...     return g
>>> f = inc_f(3)
>>> f(6)
9
>>> d = {1: f}
>>> d[1](3)
6

import
------
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

