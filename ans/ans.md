# PHP基礎 演習問題（解答例）

## 演習1（ex01.php）

```php
<?php
$a = 10;
$b = 20;

$c = $a;
$a = $b;
$b = $c;

echo '$a = ' . $a . PHP_EOL;
echo '$b = ' . $b . PHP_EOL;
?>
```

<br>

## 演習2（ex02.php）

```php
<?php
echo '点数を入力してください。' . PHP_EOL;
$stdin = trim(fgets(STDIN));

if ($stdin >= 80) {
    echo "優良";
} elseif ($stdin >= 50) {
    echo "良";
} elseif ($stdin >= 30) {
    echo "可";
} else {
    echo "不可";
}
?>
```

<br>

## 演習3（ex03.php）

```php
<?php
echo '点数を入力してください。' . PHP_EOL;
$stdin = trim(fgets(STDIN));

if ($stdin % 3 === 0) {
    echo "3の倍数" . PHP_EOL;
}
if ($stdin % 5 === 0) {
    echo "5の倍数" . PHP_EOL;
}
if ($stdin % 7 === 0) {
    echo "7の倍数" . PHP_EOL;
}
if ($stdin % 11 === 0) {
    echo "11の倍数" . PHP_EOL;
}
?>
```

<br>

## 演習4（ex04.php）

```php
<?php
echo '年齢：';
$age = trim(fgets(STDIN));
echo '学生証：';
$card = trim(fgets(STDIN));

if ($age < 20 || $card) {
    echo "1200円";
} elseif ($age >= 65) {
    echo "1500円";
} else {
    echo "1800円";
}
?>
```

<br>

## 演習5（ex05.php）

```php
<?php
$sum = 0;
for ($i = 1; $i <= 100; $i++) {
    $sum += $i;
    echo $sum . PHP_EOL;
}
?>
```

<br>

## 演習6（ex06.php）

```php
<?php
$sum = 0;
for ($i = 1; $i <= 100; $i++) {
    if ($i % 2 === 0) {
        $sum += $i;
    }
}
echo $sum . PHP_EOL;
?>
```

<br>

## 演習7（ex07.php）

```php
<?php
$scores = [80, 72, 64, 81, 90, 56, 79, 92, 43, 78];

$max = 0;
foreach ($scores as $score) {
    if ($max < $score) {
        $max = $score;
    }
}

echo "最大：$max" . PHP_EOL;
?>
```

<br>

## 演習8（ex08.php）

```php
<?php
$values = [50, 23, -64, 38, -10, 13, 41, -35, -5, 26];

$sum = 0;
foreach ($values as $value) {
    if ($value < 0) {
        $sum += $value * -1;
    } else {
        $sum += $value;
    }
}

echo "合計：$sum" . PHP_EOL;
?>
```

<br>

## 演習9（ex09.php）

```php
<?php
$fruits = ["apple" => 150, "banana" => 50, "strawberry" => 500,
           "muscat" => 1000, "pineapple" => 400];

$fruit = "";
$max = 0;
foreach ($fruits as $key => $price) {
    if ($max < $price) {
        $fruit = $key;
        $max = $price;
    }
}

echo "高額なフルーツ：$fruit $max" . "円" . PHP_EOL;
?>
```

<br>

## 演習10（ex10.php）

```php
<?php
$fruits = [1 => ["name" => "apple", "price" => 150, "quantity" => 5],
           2 => ["name" => "banana", "price" => 50, "quantity" => 20],
           3 => ["name" => "pineapple", "price" => 400, "quantity" => 2],
           4 => ["name" => "apple", "price" => 100, "quantity" => 3],
           5 => ["name" => "strawberry", "price" => 500, "quantity" => 3],
           6 => ["name" => "banana", "price" => 40, "quantity" => 10]];

echo "フルーツを入力してください。" . PHP_EOL;
$stdin = trim(fgets(STDIN));

$sum = 0;
$exist = false;
foreach ($fruits as $fruit) {
    if ($stdin == $fruit["name"]) {
        $sum += $fruit["price"] * $fruit["quantity"];
        $exist = true;
    }
}

if ($exist) {
    echo "合計：$sum" . "円" . PHP_EOL;
} else {
    echo "存在しません。" . PHP_EOL;
}
?>
```

<br>

## 演習11（ex11.php）

```php
<?php
echo '数値を入力してください。' . PHP_EOL;

$sum = 0;
while (true) {
    $stdin = trim(fgets(STDIN));
    if ($stdin == null) {
        break;
    }
    $sum += $stdin;
}

echo "合計：$sum";
?>
```

<br>

## 演習12（ex12.php）

```php
<?php
for ($i = 0; $i < 3; $i++) {
    for ($j = 0; $j < 5; $j++) {
        echo "★";
    }
    echo PHP_EOL;
}
?>
```

<br>

## 演習13（ex13.php）

```php
<?php
for ($i = 1; $i <= 5; $i++) {
    for ($j = 0; $j < $i; $j++) {
        echo "★";
    }
    echo PHP_EOL;
}
?>
```

<br>

## 演習14（ex14.php）

```php
<?php
for ($i = 0; $i < 5; $i++) {
    for ($j = 0; $j < 5 - $i; $j++) {
        echo "★";
    }
    echo PHP_EOL;
}
?>
```

<br>

## 演習15（ex15.php）

```php
<?php
for ($i = 1; $i <= 5; $i++) {
    for ($j = 0; $j < 5 - $i; $j++) {
        echo "　";
    }
    for ($j = 0; $j < $i; $j++) {
        echo "★";
    }
    echo PHP_EOL;
}
?>
```

<br>

## 演習16（ex16.php）

```php
<?php
$star = 1;
for ($i = 1; $i <= 5; $i++) {
    for ($j = 0; $j < 5 - $i; $j++) {
        echo "　";
    }
    for ($j = 0; $j < $star; $j++) {
        echo "★";
    }
    echo PHP_EOL;
    $star += 2;
}
?>
```

<br>

## 演習17（ex17.php）

```php
<?php
for ($i = 1; $i <= 9; $i++) {
    for ($j = $i; $j <= 9; $j++) {
        echo $i;
    }
    echo PHP_EOL;
}
?>
```

<br>

## 演習18（ex13.php）

```php
<?php
function printStar($count) {
    for ($j = 0; $j < $count; $j++) {
        echo "★";
    }
    echo PHP_EOL;
}

for ($i = 1; $i <= 5; $i++) {
    printStar($i);
}
?>
```

<br>

## 演習19（ex19.php）

```php
<?php
function login($id, $pass) {
    if ($id === "user01" && $pass === "pass01") {
        return true;
    }
    return false;
}

echo 'ログインID：';
$id = trim(fgets(STDIN));
echo 'パスワード：';
$pass = trim(fgets(STDIN));

if (login($id, $pass)) {
    echo "ログイン成功！！";
} else {
    echo "ログイン失敗";
}
?>
```

<br>

## 演習20（ex20.php）

```php
<?php
echo '数値を入力してください。' . PHP_EOL;

$array = [];
while (true) {
    $stdin = trim(fgets(STDIN));
    if ($stdin == null) {
        break;
    }
    array_push($array, $stdin);
}

for ($i = 1; $i <= count($array); $i++) {
    for ($j = 0; $j < count($array) - $i; $j++) {
        if ($array[$j] > $array[$j + 1]) {
            $temp = $array[$j + 1];
            $array[$j + 1] = $array[$j];
            $array[$j] = $temp;
        }
    }
}

var_dump($array);
?>
```

<br>

## 演習21（ex21.php）

```php
<?php
$hand = [1 => "グー", 2 => "チョキ", 3 => "パー"];

echo '1から3の数値を入力してください。（1：グー、2：チョキ、3：パー）' . PHP_EOL;

$player = trim(fgets(STDIN));
if (!($player >= 1 && $player <= 3)) {
    echo "入力値が不正です。" . PHP_EOL;
    exit;
}
$computer = rand(1, 3);

echo "プレイヤー：$hand[$player]" . PHP_EOL;
echo "コンピュータ：$hand[$computer]" . PHP_EOL;
if (($player == 1 && $computer == 2) ||
    ($player == 2 && $computer == 3) ||
    ($player == 3 && $computer == 1)) {
    echo "プレイヤーの勝ち" . PHP_EOL;
} elseif ($player == $computer) {
    echo "あいこ" . PHP_EOL;
} else {
    echo "コンピュータの勝ち" . PHP_EOL;
}
?>
```

<br>

## 演習22（ex22.php）

```php
<?php
$hand = [1 => "グー", 2 => "チョキ", 3 => "パー"];

$ply_win = 0;
$com_win = 0;
while (true) {
    echo '1から3の数値を入力してください。（1：グー、2：チョキ、3：パー）' . PHP_EOL;

    $player = trim(fgets(STDIN));
    if (!($player >= 1 && $player <= 3)) {
        echo "入力値が不正です。" . PHP_EOL;
        echo PHP_EOL;
        continue;
    }
    $computer = rand(1, 3);

    echo "プレイヤー：$hand[$player]" . PHP_EOL;
    echo "コンピュータ：$hand[$computer]" . PHP_EOL;
    if (($player == 1 && $computer == 2) ||
        ($player == 2 && $computer == 3) ||
        ($player == 3 && $computer == 1)) {
        $ply_win++;
    } else {
        $com_win++;
    }
    echo "プレイヤー $ply_win" . "勝：コンピュータ $com_win" . "勝" . PHP_EOL;
    echo PHP_EOL;

    if ($ply_win >= 3 || $com_win >= 3) {
        break;
    }
}

if ($ply_win >= 3) {
    echo "プレイヤーの勝利！" . PHP_EOL;
} else {
    echo "コンピュータの勝利！" . PHP_EOL;
}
?>
```

<br>

## 演習23（ex23.php）

```php
<?php
$sum = 0;
$handle = fopen("ex23_scores.csv", "r");
while ($line = fgets($handle)) {
    $scores = explode(",", $line);
    $max = 0;
    foreach ($scores as $score) {
        $score = intval($score);
        if ($max < $score) {
            $max = $score;
        }
    }
    $sum += $max;
}
fclose($handle);
echo "合計：$sum" . PHP_EOL;
?>
```

<br>

## 演習24（ex24.php）

```php
<?php
$handle_in = fopen("ex24_scores.csv", "r");
if ($handle_in === false) {
    die("INファイルオープン失敗" . PHP_EOL);
}
$handle_out = fopen("ex24_averages.csv", "w");

while ($line = fgets($handle_in)) {
    $scores = explode(",", $line);
    $sum = 0;
    foreach ($scores as $key => $score) {
        if ($key === 0) {
            fwrite($handle_out, $score . ",");
        }
        if ($key !== 0) {
            $sum += intval($score);
        }
    }
    fwrite($handle_out, $sum / (count($scores) - 1) . PHP_EOL);
}

fclose($handle_in);
fclose($handle_out);
?>
```

<br>

## 演習25（ex25.php）

```php
<?php
$handle_in = fopen("ex25_file_a.csv", "r");
if ($handle_in === false) {
    die("INファイルオープン失敗" . PHP_EOL);
}
$handle_out = fopen("ex25_file_b.csv", "w");

$total = 0;
$prefecture = "";
while ($line = fgets($handle_in)) {
    $data = explode(",", $line);
    if ($prefecture === "") {
        $prefecture = $data[0];
    } elseif ($prefecture !== $data[0]) {
        fwrite($handle_out, $prefecture . ":" . $total . PHP_EOL);
        $total = 0;
    }
    $total += intval($data[2]);
    fwrite($handle_out, $data[0] . "," . $data[1] . "," . $data[2]);

    $prefecture = $data[0];
}
fwrite($handle_out, $prefecture . ":" . $total . PHP_EOL);

fclose($handle_in);
fclose($handle_out);
?>
```
