---
title: Kotlinの基礎 1
---

## 注意

- 初心者向けの講習なので、理解を簡単にするために不正確な説明をする場合があります(というか沢山する気でいます)

- Kotlinを以下の環境で使います
- [Kotlin Playground](https://play.kotlinlang.org/#eyJ2ZXJzaW9uIjoiMS45LjIzIiwicGxhdGZvcm0iOiJqYXZhIiwiYXJncyI6IiIsIm5vbmVNYXJrZXJzIjp0cnVlLCJ0aGVtZSI6ImlkZWEiLCJjb2RlIjoiLyoqXG4gKiBZb3UgY2FuIGVkaXQsIHJ1biwgYW5kIHNoYXJlIHRoaXMgY29kZS5cbiAqIHBsYXkua290bGlubGFuZy5vcmdcbiAqL1xuZnVuIG1haW4oKSB7XG4gICAgcHJpbnRsbihcIkhlbGxvLCB3b3JsZCEhIVwiKVxufSJ9)

---

## 変数

- 数値や文字列などを持つことができる箱のこと
- 変数に値を入れることを**代入**という

<br/>

```kotlin

val 変数名 = 値
var 変数名 = 値

具体例
val name = "namakero"
var age = 19

```

<br/>

- val: 一度値を入れたら他の値を入れることができない
- var: 何度でも変えられるのだ🕶

<br/>

---

## 関数 1

<br/>

### 関数

- 処理を一纏めにしたもの
- 入力を受け取って処理し、それに応じた出力結果を返すもの

<br/>

```kotlin
fun 関数名(引数){
    処理内容
}

具体例
fun printHoge(hoge: String){
    println(hoge)
}
```

<br/>

---

### main関数

- (必ずしもそうではないが)一番最初に実行される関数

<br/>

```kotlin
fun main(引数){
    処理内容
}

具体例
fun main(){
    val name = "namakero"
    println("I am ${name}.")
}
```

<br/>

---

## 型

- 変数に入れる値の種類を見分けるためのもの
- 安全(エラーがない)なコードを書くことができる

<br/>

```kotlin
 val 変数名 : 型 = 値
 
 具体例
 var Aさん : A型 = A型の血液 //OK!
 var Aさん : A型 = B型の血液 //それはアカン! エラー!!
```

<br/>

- 型には様々な種類がある
- 自分で型を作成することができる

<br/>

```kotlin
 val a: Int = 10
 val b: Double = 10.0
 val c: String = "10" //'10'でもOK!
 val d: Boolean = true
 val e: Array<Int> = arrayOf(10, 100, 1000)
 val f: List<String> = listOf("10", "100", "1000")
 ...
```

<br/>

---

## 型推論

- 変数を使用する場合、以下の二通りの記述方法がある。

<br/>

```kotlin
宣言
val 変数名: 型

初期化
val 変数名 = 値
```

<br/>

- Q, 型書いていないのになぜエラーが出ないの？
- A, 型推論があるからじゃ
- 型を明示的に宣言していなくても、コンパイラが何の型かを理解してくれる

<br/>

---

## 問題

- 1. 自分の名前を出力してみよう!
- 2. 変数に自分の名前を代入し、それを使って自己紹介を出力してみよう!

<details>
<summary>ヒント</summary>
1. main関数内にprintln()を使用する<br/>
2. 変数を使用して出力する際は文字列フォーマット(${})を用いると楽http://localhost:4321/one/01-whatiskotlin/