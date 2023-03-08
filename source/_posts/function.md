---
title: 函式
catagories:
  - 演算法
mathjax: true
excerpt: false
date: 2023-03-08 14:09:20
---
### 前言

想像一下，如果一件事情要在程式裡面一直重複，要如何寫呢

> 重複貼很多次？

或許不是個好方法。這樣的缺點是會讓程式變很長，並且難以找到錯誤。

所以，我們常會利用函式來簡化程式碼  

函式可以將重複的事情包裝起來，增加程式的可讀性

### 寫法

C++中的函式宣告長這樣

```c++=
int sum(int a, int b){
    int ans = a + b;
    return ans;
}
```
下面將會介紹各區塊的寫法及用途

{% folding blue::int sum %}

其中的int代表這個函式回傳值的類型，可為bool, int, long long, char, string等等，或者是不回傳，用void開頭

回傳值甚至可以是陣列或其他資料結構，但比較麻煩跟複雜，實際上比較不常用。

而sum則是這個函式的名稱，要注意不可以跟現有的關鍵字相同，否則會出現錯誤。

{% endfolding %}

{% folding blue::(int a, int b) %}

a, b為傳入的參數，為這個函式的區域變數

{% endfolding %}

{% folding blue::int ans = a + b;%}

函式內可以做的事情跟主程式一樣，可以輸入輸出、宣告變數等。

{% endfolding %}

{% folding blue::return ans;%}

函式最後需要一個回傳值，須和一開始設定的相同  

若函式為void函式，可選擇不回傳或以下兩種方式結束函式
```c++=
return;
return void();
```

{% endfolding %}

函式使用範例如下列程式
```c++=
#include<iostream>
using namespace std;
int sum(int a, int b){
    int ans = a + b;
    return ans;
}
int main(){
    int x, y;
    cin >> x >> y;
    cout << sum(x, y) << endl;
    return 0;
}
```