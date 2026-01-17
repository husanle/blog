---
permalink: /YACS1146-answer/
layout: default
---

# [YACS1146水面之下](https://www.iai.sh.cn/problem/1146)

*题意*：看动画片，有一些谜团，当现有的谜团全部被解决，总共天数就增加了1天。

*输入*：输入一行一个整数 n，表示动画有多少集。接下来一行n个整数 a1,a2,...,an，表示第i集的谜团在ai集解释。

*思路*：注意`a`的长度`<=100000`,可以用一个变量`max_a`储存最后一个谜团，当看到`max_a`集时，`天数+1`。

```
#include<bits/stdc++.h>
using namespace std;
int main()
{
    int n;
    cin>>n;
    vector<int> a(n+1);
    int max_a=0,cnt=0;
    for(int i=1;i<=n;i++)
    {
        cin>>a[i];
    }
    for(int i=1;i<=n;i++)
    {
        max_a=max(max_a,a[i]);
        if(i==max_a)
        {
            cnt++;
        }
    }
    cout<<cnt;
    return 0;
}
```