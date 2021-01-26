# KAHOOT
## 10/23
[![hackmd-github-sync-badge](https://hackmd.io/T5-qbHHqTg6voLLAyZODcA/badge)](https://hackmd.io/T5-qbHHqTg6voLLAyZODcA)
### Q1 Which is correct ?
1.
![](https://i.imgur.com/P9aHIuw.jpg)
* 單純考你**陣列的索引順序**
 [review Array](https://hackmd.io/PbClBLHOROiMKHCZLhsyvg)
### Q2 看輸出
![](https://i.imgur.com/rwBXQQT.jpg)
其實不複雜,就一個**while迴圈** ++由後往前++ (再這邊由前往後或後往前不影響)看陣列**當前的元素**是否為==偶數==,若為偶數**sum**加1
其實不複雜,就一個**while迴圈** ++由後往前++ (再這邊由前往後或後往前不影響)看陣列**當前的元素**是否為**偶數**,若為偶數**sum**加1

### Q3 看輸出
![](https://i.imgur.com/k8DezJ5.jpg)
跟上一題差不多的概念,也是==判斷偶數==,不過改為**for迴圈**,再加入**continue**的概念 (遇到時,跳過接下來的內容,跑下一個迴圈)
跟上一題差不多的概念,也是**判斷偶數**,不過改為**for迴圈**,再加入**continue**的概念 (遇到時,跳過接下來的內容,跑下一個迴圈)

不過,加了**小陷阱**!
++斷判偶數++的**if**位於`sum+=i;`之後
所以==不會跳過偶數==
所以**不會跳過偶數**

### Q4 看輸出
![](https://i.imgur.com/37bvbcY.jpg)
比起前幾題,可能稍微複雜一些
利用兩個**for迴圈**,判斷陣列中的元素==是否相同==,並求==第二層for迴圈需++幾次==:
++第一層++的**for迴圈**會先抓出findlist的++第i個元素++,接者++第二層++的for抓出numlist的++第j個元素++與`findlist[i]`比較,當兩陣列的元素相同時,==結束第二層迴圈==
**第一層**的**for迴圈**會先抓出findlist的**第i個元素**,接者**第二層**的for抓出numlist的**第j個元素**與`findlist[i]`比較,當兩陣列的元素相同時,**結束第二層迴圈**

### Q5 看輸出
![](https://i.imgur.com/8ugLvpz.jpg)
考**二維陣列**的輸入輸出:
arr為2X3的陣列所以用++第一層為2++,++第二層為3++的**for迴圈**做輸入輸出
不過輸出的**第二層迴圈**是==反向輸出==
arr為2X3的陣列所以用**第一層為2**,**第二層為3**的**for迴圈**做輸入輸出
不過輸出的**第二層迴圈**是**反向輸出**
所以結果為


@@ -47,14 +48,14 @@ numlist的permanent控制函式內for迴圈的**乘積(i*N)**
### Q8 看輸出
![](https://i.imgur.com/IxZ1l1g.jpg)
也是函式,不過重點在**for迴圈**:
從後往前,==當前的元素*=前一個元素==
從後往前,**當前的元素** *=前一個元素==
Eg i=4時:
lis[4]=lis[4]*lis[3]
而**原本的**lis[4]值為5,lis[3]值為5
所以**新的**lis[4]為25
### Q9 num為多少才會return 7
![](https://i.imgur.com/6kaToCW.jpg)
在**while(num)**,只要++num>0++,
迴圈就==不會停下來==
迴圈就**不會停下來**
而`else if(lis[num]&&(num-2))`中:
只要lis[num]不是0就代表`true`,(num-2)不是0就代表`ture`再**取交集做判斷**
只要lis[num]不是0就代表`true`,(num-2)不是0就代表`ture`再**取交集做判斷**
