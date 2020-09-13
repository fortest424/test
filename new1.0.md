 c++
 ===
 ## 型態
> :::spoiler  **int**
> int：整數型態
>```int
>int num;              //單純宣告變數num
>int num1=25;         //宣告num1為25
>```
> 
>int 的範圍:-2,147,483,648 至 2,147,483,647
> :::
> :::spoiler  **char**
> char：只是一個字元而已
>```int
>char a;             //單純宣告變數a
>char b='b';         //宣告b為'b'```
>記得是單引號''喔喔喔
>()
> :::
> :::spoiler  **float**
> float：浮點數型態(有小數點)
>```int
>float F;             //單純宣告變數F`
>float FF=3.14159;     //宣告FF為3.14159
>``` 
>可至小數點後7位
> :::
> :::spoiler  **string**
> string："字串"型態 (一個char陣列的概念)
>```int
>string str;             //單純宣告變數str`
>string str1="wlsh";         //宣告str1為wlsh`
>```
>記得是雙引號""喔喔喔喔
> :::
> :::spoiler **bool**
> bool:布林值(用來表達對或錯)
> ```int
> bool identify=true;     //其實true就是1
> bool identify=false;    //而false就是0
> ```
> :::
### 額外補充
:::spoiler  **數不大何以聚人心!!!**
 int 只到 2,147,483,647 
 float 只到小數點後7位
 
 如果要處理12,345,678,910呢??
 或3.1415926535呢??
 :::spoiler  **今晚我想來點...**
* long long
範圍:-9,223,372,036,854,775,808 至 9,223,372,036,854,775,807
* double
可至小數點後15位
:::spoiler **可是...這樣不能處理跟我一樣大的數字啊**
**Soultion**
1.Python 
2.大數運算
:::
 ## 基本輸出&輸入
>:::spoiler **cin**
>**語法:cin>>變數名稱;**
>`cin>>num;`
>:::danger 
>cin時:遇到空白鍵或換行符號就會停止喔喔喔!!
>:::
>:::spoiler **cout**
>**語法:cout<<變數名稱;**
>```int
>cout<<7122;//單純輸出7122
>cout<<num;//輸出num裡面的data
>```
>**我想要換行:**
>```int
>cout<<"\n";//BTW"\n"的執行速度會比endl還快ㄛ
>cout<<"endl";
>```
>:::
484很簡單呢?
### 額外補充
:::spoiler **多人運動?**
:::spoiler **如果別人輸入:"1 2 3 4 5",但我想讀取整行 .___.**
*  getline
```int
/*Example*/
string str1;
string str2;
getline(cin,str1);   //input:1 4 6 4 1
cin>>str2;           //input:1 3 3 1
cout<<str1<<"\n";    //output:1 4 6 4 1
cout<<str2<<"\n";    //output:1
```
:::
## 四則運算&字元處理
>:::spoiler **四則運算**
> * 加法:+
> ```int
> int a=8,b=9;
> cout<<a+b;//17
> ```
> * 減法:-
> ```int
> int a=8,b=9;
> cout<<a-b;//-1
> ```
> * 乘法:*
> ```int
> int a=8,b=9;
> cout<<a*b;//72
> ```
> * 除法:/
> ```int
> int a=8,b=9;
> cout<<a/b;//0
> ```
> * 取餘數:%
> ```int
> int a=3,b=2;
> cout<<a%b;//1
> ```
> :::spoiler **剛剛提到的大數...?**
>**Soultion**
>1.Python (因為py內建有大數運算!!)
>2.大數運算  :這個我們下次影片講解(~~老高口音~~
>是因為這次講義內容真的不夠我們解決這個問題啦...
>:::
>
>:::spoiler **字元處理**
>如果:
>```int
>char a='8',b='9';
>cout<<a+b;
>```
>會輸出17嗎?
>:::spoiler **char轉int?**
> * ASCII碼 [ASCII](https://zh.wikipedia.org/zh-tw/ASCII)
> 簡而言之:每個字元都有一個號碼代表(例如A的ASCII為65)
> * 語法:(int)'字元'得到該字元的ASCII碼
>For example:
> ```int
> cout<<(int)'a';//61
> ```
> 那剛剛這題...?
> ```int
> cout<<((int)'8'-(int)'9');//就可以啦!!
> ```
> 如果單純要值...?
> ```int
> cout<<((int)'8'-(int)'0');//8
> ```
大家都懂了嗎??
### 額外補充
:::spoiler **我全都要?**
:::spoiler **如果別人輸入"59487",我也需要這樣慢慢換嗎?**
* stringstream
要先`#include<sstream>`
跟`cin`和`cout`一樣:都具備`>>`,`<<`串流運算子
**基本操作:** 詳細參照[C++reference](http://www.cplusplus.com/reference/sstream/stringstream/?kw=stringstream)
```int
stringstream ss;      
string Str="59487";
int num;
ss.str(Str);      //將Str放入stringstream流
ss>>num;         //num為int型態,值:59487
ss.clear()      //將stringstream清空
cout<<num+1;   //59488
```
:::spoiler **額外補充的額外補充!**
* stringstream還可以處理:"1 2 3 4 5"這種含空格的字串
* 常搭配getline使用
```int
string Str,temp;
stringstream ss;
getline(cin,Str);     //假設輸入"1 2 3 4 5"
ss.str(Str);          //ss:"1 2 3 4 5"
ss>>temp;             //temp:1
cout<<temp;           //1
ss>>temp;             //temp:2
cout<<temp;           //2
/*可搭配之後要交的迴圈使用*/
```
:::
## if-else判斷
> :::spoiler **判斷?**
> * : 如果...就...
> Eg;如果(你有女朋友)就(一定是假的)
> :::
> :::spoiler **關係運算子**
> * 1. `==` (有兩個"="喔!)
> meaning:equal
>  ```int
>  int a=1;               //assign a=1
>  if(a==1) cout<<"a=1";  //如果a等於1,輸出"a=1"
>  ```
> * 2. `<`
> :小於
> * 3. `>`
> :大於
> * 4. `<=`
> :小於等於
> * 5. `>=`
> :大於等於
> :::
> :::spoiler **邏輯運算子**
> * 1. ! (這是驚嘆號)
> meaning:not
> ```int
> string school;
> cin>>school;       //cin:CKHS
> if(school!="wlsh"){
>    cout<<"SUCK"; //沒有啦他們一堆國手電神,惹不起啊= =
>} 
> ```
> * 2. || (在鍵盤backspace的下方)
> meaning:or
> 取聯集,或
> ```int
> /*example*/
> int math,mandarin;
> if(math>90||mandarin>90){ //判斷式
>    cout<<"It's impossible"; 
>} 
> ```
> * 3. && 
> meaning:and
> 取交集,且
> ```int
> bool girlfriend=true;
> string you=programmer;
> if(girlfriend==true&&you=="programmer"){
>    cout<<"She must be in your imagination._."
>}
> ```
> :::
> 
> 
> :::spoiler **in C++...**
>  :::spoiler **那else呢??**
>  else:做不符合判斷式的事
>  ```int
>  int score=59;
>  if(score>=60){
>    cout<<"You pass!!";
>  }
>  else{
>    cout<<"poor guy";      //可憐啊 
>  }
>  ```
>  **啊我想判斷很多東西咧??**
>  :::spoiler **巢狀if-else**
>  在else中在放入if   (什麼意思??)
>  看Code一目了然
>  ```int
>  int score=41;
>  if(score>=60){
>      cout<<"We did it!We did it!";
>  }
>  else{
>      if(score>=40){
>          cout<<"還有救啦...應該吧?";
>      }
>      else{
>          cout<<"揪團補修去";
>      }
>  }
>  ```
>  :::spoiler **else if?**
>  else if()
>  Why:就比較方便啊
>  像剛剛的可以表示成...
>  ```int
>  int score=41;
>  if(score>=60){
>      cout<<"We did it!We did it!";
>  }
>  else if(score>=40){
>      cout<<"還有救啦...應該吧?";
>  }
>  else{
>      cout<<"揪團補修去";
>  }
>  ```
>  :::
### 額外補充
:::spoiler **AM I JOKING YOU?**
呵...這邊沒有要補充的
:::
### Preview
:::spoiler **不勉強,心有餘力可以預習**
* while 迴圈
* for 迴圈
* array
* function
:::













