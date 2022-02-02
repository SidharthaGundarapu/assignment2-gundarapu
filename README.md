# Sidhartha Gundarapu

## Paradise is my favourite place to buy food

As i love having **tasty** food. And the **Paradise** biryani has the option of takeaway, home delivery and dine in. It also makes various flavours of the **biryani's.**

To become familiar with markdown

---

### DIRECTION'S FROM AIRPORT TO PARADISE

The closest airport to the Paradise is Rajiv Ghandi International Airport, Hyderabad.

1. After landing at airport we have many optiong to travel from the airport to paradise hotel, they are
   1. Take a cab/taxi
   2. Rent a car
   3. Any contact can recieve
   4. Take public transport
2. After the decision of the way of transport we can easily travel from airport to  paradise hotel.
3. And in the way we can have an excellent view of the sky-scrapers and the ORR-Nehuru Outer Ringroad.
4. Also we can see the flyovers, shoping malls, the business markets, software offices and parade ground, US embassy and finally reach paradise hotel for having a tasty meal.

-There are various food items in paradise menu, they are:

-Biryani's
-Kebab's
-Dessert's
-Beverage's
-And i would recommend others to have the biryani as it is famous.
[AboutMe](https://github.com/SidharthaGundarapu/assignment2-gundarapu/blob/main/AboutMe.md)

---

#### Table Section

---

The Table gives the information of gamename, location, money for the equipment.

| Game Name | Location      | Money |
| --------- | ------------- | ----- |
| Cricket   | Wankhede      | 250$  |
| Football  | Manchester    | 200$  |
| Pingpong  | Lion's club   | 150$  |
| Golf      | The Golf club | 100$  |

---

##### Quote Section

---

> "Mathematicians deal with large numbers sometimes, but never in their income".

*Issac Asimov*

> “One doesn't expect a falcon to pull a plow, or a butterfly to cook your breakfast”.

*Katherine Blake*

---

Code Fencing
------------

> There are many algorithms for processing strings, each with various trade-offs. Competing algorithms can be analyzed with respect to run time, storage requirements, and so forth.
> Some categories of algorithms include:
> String searching algorithms for finding a given substring or pattern
> String manipulation algorithms
> Sorting algorithms
> Regular expression algorithms
> Parsing a string
> Sequence mining
> Advanced string algorithms often employ complex mechanisms and data structures, among them suffix trees and finite-state machines.
> The name stringology was coined in 1984 by computer scientist Zvi Galil for the issue of algorithms and data structures used for string processing.
> [Quicklink](https://en.wikipedia.org/wiki/String_(computer_science))

```
Implementation:
const int N=1000000,INF=1000000000;
string a;
int t[N][26],l[N],r[N],p[N],s[N],tv,tp,ts,la;

void ukkadd (int c) {
    suff:;
    if (r[tv]<tp) {
        if (t[tv][c]==-1) { t[tv][c]=ts;  l[ts]=la;
            p[ts++]=tv;  tv=s[tv];  tp=r[tv]+1;  goto suff; }
        tv=t[tv][c]; tp=l[tv];
    }
    if (tp==-1 || c==a[tp]-'a') tp++; else {
        l[ts+1]=la;  p[ts+1]=ts;
        l[ts]=l[tv];  r[ts]=tp-1;  p[ts]=p[tv];  t[ts][c]=ts+1;  t[ts][a[tp]-'a']=tv;
        l[tv]=tp;  p[tv]=ts;  t[p[ts]][a[l[ts]]-'a']=ts;  ts+=2;
        tv=s[p[ts-2]];  tp=l[ts-2];
        while (tp<=r[ts-2]) {  tv=t[tv][a[tp]-'a'];  tp+=r[tv]-l[tv]+1;}
        if (tp==r[ts-2]+1)  s[ts-2]=tv;  else s[ts-2]=ts; 
        tp=r[tv]-(tp-r[ts-2])+2;  goto suff;
    }
}

void build() {
    ts=2;
    tv=0;
    tp=0;
    fill(r,r+N,(int)a.size()-1);
    s[0]=1;
    l[0]=-1;
    r[0]=-1;
    l[1]=-1;
    r[1]=-1;
    memset (t, -1, sizeof t);
    fill(t[1],t[1]+26,0);
    for (la=0; la<(int)a.size(); ++la)
        ukkadd (a[la]-'a');
}
```

[Source Code](https://cp-algorithms.com/string/suffix-tree-ukkonen.html)
