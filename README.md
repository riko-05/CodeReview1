# 第一回　ATGS社内勉強会　コードレビュー会
問題文はAtCoder様で開催されたコンテストの過去問より出題しています。  
https://atcoder.jp/

# 問題文
すぬけ君は1〜Nの整数が等確率で出るN面サイコロと表と裏が等確率で出るコインを持っています。すぬけ君は、このサイコロとコインを使って今から次のようなゲームをします。

1. まず、サイコロを1回振り、出た目を現在の得点とする。
2. 得点が1以上K−1以下である限り、すぬけ君はコインを振り続ける。表が出たら得点は2倍になり、裏が出たら得点は0になる。
3. 得点が0になった、もしくはK以上になった時点でゲームが終了する。このとき、得点がK以上である場合すぬけ君の勝ち、0である場合すぬけ君の負けである。

NとKが与えられるので、このゲームですぬけ君が勝つ確率を求めてください。

# 制約
- 1≤N≤10^5
- 1≤K≤10^5
- 入力はすべて整数

# 入力
入力は以下の形式で標準入力から与えられる。
```
N K
```

# 出力
すぬけ君が勝つ確率を出力せよ。絶対誤差または相対誤差が 
10^−9以下のとき正解とみなされる。

# 入力例 1 
```
3 10
```

# 出力例 1 
```
0.145833333333
```
サイコロの出た目が1のとき、得点が10以上になるためには、4回コインを振って4連続で表が出る必要があります。  
この確率は、1/3×(1/2)^4=1/48です。  
サイコロの出た目が2のとき、得点が10以上になるためには、3回コインを振って3連続で表が出る必要があります。  
この確率は、1/3×(1/2)^3=1/24です。  
サイコロの出た目が3のとき、得点が10以上になるためには、2回コインを振って2連続で表が出る必要があります。  
この確率は、1/3×(1/2)^2=1/12です。  
よって、すぬけ君が勝つ確率は、1/48+1/24+1/12=7/48≃0.1458333333です。

# 入力例 2 
```
100000 5
```

# 出力例 2 
```
0.999973749998
```
