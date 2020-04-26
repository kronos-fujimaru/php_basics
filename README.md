# アルゴリズム演習問題

C:￥itc￥php_exフォルダを作成し、各演習をPHPファイルを作成しなさい。

## 演習1（ex01.php）
変数aと変数bに格納されている値を入れ替え、値を表示しなさい。

```php
<?php
$a = 10;
$b = 20;

???
?>
```

**出力結果**

```
$a = 20
$b = 10
```

<br>

## 演習2（ex02.php）
標準入力で点数（整数値）を入力させ、80以上は「優」、50点以上80点未満は「良」、30点以上50点未満は「可」、30点未満は「不可」を表示しなさい。

> PHPでは、fgets(STDIN) で標準入力ができる。

```php
<?php
echo '点数を入力してください。' . PHP_EOL;
$stdin = trim(fgets(STDIN));

???
?>
```

**出力結果**

```
点数を入力してください。
80
優
```

<br>

## 演習3（ex03.php）
標準入力で数値を入力させ、数値が3の倍数の時は "3の倍数"、数値が5の倍数の時は "5の倍数"、数値が7の倍数の時は "7の倍数"、数値が11の倍数の時は "11の倍数"と表示しなさい。例えば、入力された数値が231の場合は、"3の倍数"と"7の倍数"と"11の倍数"を表示する。

**出力結果**

```
整数を入力してください。
231
3の倍数
7の倍数
11の倍数
```

<br>

## 演習4（ex04.php）
標準入力で年齢、学生証（0:無、1:有）を入力させ、以下のように金額を表示しなさい。

- 20歳以上は、1800円
- 65歳以上は、1500円
- 20歳未満または学生証を持っている人は、1200円

**出力結果**

```
年齢：25
学生証：1
1200円
```

<br>

## 演習5（ex05.php）
1から100までの数値を順に足した結果を表示しなさい。

**出力結果**

```
1
3
6
10
15
21
28
36
45
55
...（中略）
5050
```

<br>

## 演習6（ex06.php）
1から100の間の偶数値の総和を表示しなさい。

**出力結果**

```
合計：2550
```

<br>

## 演習7（ex07.php）
配列に格納されている数値のうち最大値を表示しなさい。

```php
$scores = [80, 72, 64, 81, 90, 56, 79, 92, 43, 78];

???
```

**出力結果**

```
最大：92
```

<br>

## 演習8（ex08.php）
配列に格納されている数値の絶対値の総和を表示しなさい。

```php
$values = [50, 23, -64, 38, -10, 13, 41, -35, -5, 26];

???
```

**出力結果**

```
合計：305
```

<br>

## 演習9（ex09.php）
連想配列に格納されているフルーツの価格のうち、一番価格の高いキー（フルーツ名）と価格を表示しなさい。

```php
$fruits = ["apple" => 150, "banana" => 50, "strawberry" => 500,
           "muscat" => 1000, "pineapple" => 400];

???
```

**出力結果**

```
高額なフルーツ：muscat 1000円
```

<br>

## 演習10（ex10.php）
二次元の連想配列にフルーツの名称、価格、数量が格納されている。標準入力でフルーツ名を入力させ、対象フルーツの合計金額を表示しなさい。指定したフルーツが存在しない場合は、"存在しません。"と表示しなさい。

```php
$fruits = [1 => ["name" => "apple", "price" => 150, "quantity" => 5],
           2 => ["name" => "banana", "price" => 50, "quantity" => 20],
           3 => ["name" => "pineapple", "price" => 400, "quantity" => 2],
           4 => ["name" => "apple", "price" => 100, "quantity" => 3],
           5 => ["name" => "strawberry", "price" => 500, "quantity" => 3],
           6 => ["name" => "banana", "price" => 40, "quantity" => 10]];

???
```

**出力結果**

```
フルーツを入力してください。
apple
合計：1050円
```

<br>

## 演習11（ex11.php）
標準入力で数値を入力させ、総和を表示しなさい。標準入力では、未入力でEnterキーが押されるまで数値を入力させる。

**出力結果**

```
数値を入力してください。
10
20
30

合計：60
```

<br>

## 演習12（ex12.php）
"★"を3行5列表示しなさい。

**出力結果**

<img src="img/ex12.png" width="300">

<br><br>

## 演習13（ex13.php）
"★"を1行目に1個、2行目に2個、・・・、5行目に5個表示しなさい。

**出力結果**

<img src="img/ex13.png" width="300">

<br><br>

## 演習14（ex14.php）
"★"を1行目に5個、2行目に4個、・・・、5行目に1個表示しなさい。

**出力結果**

<img src="img/ex14.png" width="300">

<br><br>

## 演習15（ex15.php）
"★"を出力結果のような形に表示しなさい。

**出力結果**

<img src="img/ex15.png" width="300">

<br><br>

## 演習16（ex16.php）
"★"を出力結果のような形に表示しなさい。

**出力結果**

<img src="img/ex16.png" width="300">

<br><br>

## 演習17（ex17.php）
1行目に"1"を9個、2行目に"2"を8個、・・・9行目に"9"を1個を表示しなさい。

**出力結果**

```
111111111
22222222
3333333
444444
55555
6666
777
88
9
```

<br>

## 演習18（ex18.php）
演習11同様、未入力でEnterキーを押されるまで標準入力で複数の数値を入力させ、数値を昇順（小さい値からだんだん大きい値になる順）に並べ替え、配列の中身を表示しなさい。並び替えは、隣り合う要素を最初から見ていき、大きさが逆であれば入れ替える、バブルソートとする。

**出力結果**

```
数値を入力してください。
56
90
21
45
73

array(5) {
  [0]=>
  string(2) "21"
  [1]=>
  string(2) "45"
  [2]=>
  string(2) "56"
  [3]=>
  string(2) "73"
  [4]=>
  string(2) "90"
}
```

<br>

## 演習19（ex19.php）
プレイヤーとコンピュータがジャンケンをするプログラムを作成する。<br>標準入力で1から3の数値（1：グー、2：チョキ、3：パー）を入力させ、コンピュータの手を同じく1から3の乱数で決める。プレイヤーとコンピュータの手を文字列として表示し、プレイヤーが勝ったら"プレイヤーの勝ち"、コンピュータが勝ったら"コンピュータの勝ち"、同じ手であれば"あいこ"と表示しなさい。標準入力で1から3以外の値が入力された場合は、"入力値が不正です。"と表示する。

> rand関数で乱数を生成できる。<br>https://www.php.net/manual/ja/function.rand.php

**出力結果**

```
1から3の数値を入力してください。（1：グー、2：チョキ、3：パー）
2
プレイヤー：チョキ
コンピュータ：パー
プレイヤーの勝ち
```

<br>

## 演習20（ex20.php）
演習19のジャンケンプログラムで、連続でジャンケンをし、どちらかが3勝したら終了とする。各ジャンケンで両者の勝利数を表示する。

**出力結果**

```
1から3の数値を入力してください。（1：グー、2：チョキ、3：パー）
1
プレイヤー：グー
コンピュータ：チョキ
プレイヤー 1勝：コンピュータ 0勝

1から3の数値を入力してください。（1：グー、2：チョキ、3：パー）
3
プレイヤー：パー
コンピュータ：パー
プレイヤー 1勝：コンピュータ 0勝

...（中略）

1から3の数値を入力してください。（1：グー、2：チョキ、3：パー）
2
プレイヤー：チョキ
コンピュータ：パー
プレイヤーの勝ち
プレイヤー 3勝：コンピュータ 2勝

プレイヤーの勝利！
```

<br>

## 演習21（ex21.php）
CSVファイルのデータの中で、行ごとの最高点だけを合計し表示しなさい。<br>CSVファイルは以下のリンクからダウンロードしてください。

[CSVファイルをダウンロード](attach:csv/ex21_scores.csv)

**出力結果**

```
合計：699
```
