# Python 入門

## 目次
1. プログラミング言語とはなにか
2. Pythonとはなにか
3. Pythonでできること
4. Pythonの書き方  
  
### 1. プログラミング言語とはなにか
プログラミング言語は、コンピュータに指令を出すもの。  
自分が出したい指令 -> プログラミング言語  
  
コンピュータは日本語が分からない。  
コンピュータのCPU(処理部分)は機械語でしか分からないけれども、人間にとって機械語で指令を出すのは酷。  
なので、高水準なプログラミング言語(人間にとって理解しやすい言語)で指令を出そうということ。  

CPUの処理は、「保存、計算、制御」の3つに分かれる。
保存：値をメモリ上に保存する
計算：保存した値から、さらなる値を算出する
制御：計算方法や、保存先を決める

### 2. Pythonとはなにか
プログラミング言語のひとつ。他にも以下のような言語がある。  
  
1) Ruby, PHP, JavaScript ...etc  
2) C, Java, C# ...etc   

#### インタプリタ言語とコンパイル言語
処理の流れは以下のようになっている。
コンピュータ(CPU)に処理され、実行される <- 機械語 <- コンパイル(翻訳) <- プログラミング言語  

1) インタプリタ言語 : 一行ずつコンパイルして逐次実行する(比較的遅いが、学習コストが低い)  
2) コンパイル言語　 : 一気にコンパイルしてから実行する(比較的早い、学習コストが高い)  

#### 構文のシンプルさと可読性の高さ
初学者にとって、シンタックスが読みやすくなっている。  
また、インデントによるスコープ定義により、可読性が高くなっている。  


### 3. Pythonでできること
1. 機械学習を使った人工知能の開発
2. 自動データ処理や分析などの業務効率化
3. スクレイピングによるWEB上の画像データ・テキストデータの自動収集
4. WEBサービス・WEBアプリケーション制作
5. スマホアプリ（Android）制作
6. デスクトップアプリ制作
7. 組み込みアプリケーション制作
8. フィンテック・ブロックチェーン技術の開発

応用範囲が広いため、少ない学習で多くのことができる。  
  
### 4. Pythonの書き方
1) 変数とデータ型  
```
変数宣言と初期化は「変数名 = 値」とする。
予約語は変数名に使用できない。

数値、文字列、ブール型があり、型は自動的に判定される。
リストには、複数の値をまとめて格納することができる。
他にもディクショナリ型、タプル、セットなどがある。



<main.py>
num = 1
print(num) # 1
print(type(num)) # <class 'int'>

print("")
flt = 1.1
print(flt) # 1.1 
print(type(flt)) # <class 'float'>

print("")
s = "str"
print(s) # str
print(type(s)) # <class 'str'>

print("")
b = True
print(b) # True
print(type(b)) # <class 'bool'>

print("")
fruits = ["apple", "banana", "orange"]
print(fruits[0]) # apple
print(fruits[1]) # banana
print(fruits[2]) # orange
print(type(fruits)) # <class 'list'>



$ python3 main.py
1
<class 'int'>

1.1
<class 'float'>

str
<class 'str'>

True
<class 'bool'>

apple
banana
orange
<class 'list'>

```  
  
2) 演算子  
```
算術演算子は、数値を返す。
比較演算子、等価演算子はbool型の値を返す。



<main.py>
a = 12
b = 4
c = 12

# 算術演算子
print(a + b) # 16
print(a - b) # 8
print(a * b) # 48
print(a ** b) # 20736
print(a / b) # 3.0
print(a // b) # 3
print(a % b) # 0 


# 比較演算子
print("")
print(a > b) # True
print(a < b) # False
print(a >= b) # True
print(a <= b) # False

# 等価演算子
print("")
print(a == c) # True
print(a != b) # True
print(a != c) # False

# and演算子(すべての条件がTrueなら、Trueを返す)
print("")
print(a == b and a == c) # False

# or演算子(すくなくとも一つの条件がTrueなら、Trueを返す)
print("")
print(a == b or a == c) # True



$ python3 main.py
16
8
48
20736
3.0
3
0

True
False
True
False

True
True
False

False

True

```  

```
複合代入演算子 (+=, -=, *=, /=, ...etc)



<main.py>
a = 10
b = 4

a += 10
print(a) # 20

a -= 10
print(a) # 10

a *= b
print(a) # 40

a /= b
print(a) # 10.0

a //= b 
print(a) # 2.0

a **= b
print(a) # 16.0



$ python3 main.py
20
10
40
10.0
2.0
16.0

```  
  
3) 制御構文  
```
if文：条件に従って、処理を分岐させる



<main.py>
EXPENSIVE_PRICE = 3000
MODERATE_PRICE = 1500
price = 1000

if price >= EXPENSIVE_PRICE:
    print("EXPENSIVE!!")
elif price < EXPENSIVE_PRICE and price >= MODERATE_PRICE :
    print("OK.")
else:
    print("CHEAP!!")
 
 
 
$ python3 main.py
CHEAP!!

```  
  
```
for文：指定した回数分だけ、繰り返し実行する



<main.py>
# range(5) == [0, 1, 2, 3, 4] 
for i in range(5):
  print(i)

print("------------")

for i in [1, 2, 3, 4, 5]:
  print(i)



$ python3 main.py
0
1
2
3
4
------------
1
2
3
4
5

```  
  
4) 関数  
```
関数とは、複数の処理をひとつにまとめたもの
def 関数名(仮引数1, 仮引数2, ...仮引数N) : 関数定義
関数名(実引数1, 実引数2, ...実引数N) : 関数の呼び出し
注意: インデントは4つにする(言語によって異なるけど)



<main.py>
def plus(a, b):
    return a + b

def show(a, b):
    print("a: {}, b: {}".format(a, b))

print(plus(1, 2))
show(1, 2)



$ python3 main.py
3
a: 1, b: 2

```  
  
5) クラス  
```
クラスとは
オブジェクト指向プログラミングにおいて、インスタンス(実体)の設計図となるもの。

オブジェクトとは
データと振る舞い(処理)を定義したデータ構造。

インスタンス
クラスをもとに生成されたヒープメモリ上のデータ


class Person:
    def __init__(self, height, weight):
        self.height = height
        self.weight = weight
    
    def bmi(self):
        return (self.weight / (self.weight ** 2))

done_san = Person(1.87, 74.2)
print(done_san.bmi())

$ python3 main.py
0.013477088948787061
```



