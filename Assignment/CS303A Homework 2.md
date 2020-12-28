# CS303A Homework 2

11812419 JIANG Yuchen



## Q1.

### a.

![image-20201218201638270](C:\Users\THINKPAD\AppData\Roaming\Typora\typora-user-images\image-20201218201638270.png)

​															Figure.1 Enumeration of sentence

​	As figure.1 shows, by using enumeration with all possible conditions, the sentence is always true so it's valid.



### b.

![image-20201218214939996](C:\Users\THINKPAD\AppData\Roaming\Typora\typora-user-images\image-20201218214939996.png)

​																		Figure.2 Steps of converting

As figure.2 shows, by converting, left hand equals right hand. Thus, left hand => right hand will be always true, which means it's valid and confirms the result in **a.**



### c.

To prove it by resolution, first we negate it, which is left hand can't infer right hand.

However, according to b., CNF of left hand and right hand are same, which contradict that left hand can't infer right hand. Thus, left hand can infer right hand, which is proof to **a.**





## Q2.

### a.

(i)  (2) is syntactically invalid and therefore meaningless. Because in function In(x, y) , x only represents one city so it's syntactically invalid.

(ii)  (1) correctly expresses the English sentence. It shows 'both' with two separate segments and use the correct signal.

(iii) (3) is syntactically valid but does not express the meaning of the English sentence. It not only represents 'Paris and Marseilles are both in France', but also represents 'either Paris or Marseilles is in France.', which is not accurate.



### b.

(i) (1) correctly expresses the English sentence. It restrict the country with $\and$ signal.

(ii) (3) is syntactically valid but does not express the meaning of the English sentence. It represents 'If c is a country, then c borders Iraq and Pakistan', which is wrong.

(iii) (2) is syntactically invalid and therefore meaningless. $\exists c$ shouldn't be added in left hand, which turns ‘There exists c, if c is a country, ....' into 'If there exists c, c is a country, ...', which is syntactically invalid and we can't judge whether left hand is true or not. In fact, we want it to be true, not to be judged.

(iv) (2) is syntactically invalid and therefore meaningless. In function Borders(x, y), x and y only represent one city, not two cities or even a sentence.



### c.

(i)  (1) correctly expresses the English sentence. For every c, if c is a country and c borders Ecuador, then c is in SouthAmerica.

(ii) (1) correctly expresses the English sentence. Estimating all '=>' we will find it equals (i).

​	![image-20201219004755846](C:\Users\THINKPAD\AppData\Roaming\Typora\typora-user-images\image-20201219004755846.png)

​											Figure.3  Steps of estimation

(iii) (3) is syntactically valid but does not express the meaning of the English sentence. Also after estimating, it's $\forall c [Country(c)\and (\neg Border(c,Ecuador))\or In(c,SouthAmerica)]$ ,which is different from (i).

(iv) (3) is syntactically valid but does not express the meaning of the English sentence. It means that every country borders Ecuador and is in South America.



### d.

(i)  (1) correctly expresses the English sentence. Move $\neg$ inside the sentence we will get that for every c,d, c in SouthAmerica and d in Europe and c,d border is false, which represents same meaning as No region in South America borders any region in Europe.

(ii) (1) correctly expresses the English sentence. Similar as (i), c,d border is false.

(iii) (3) is syntactically valid but does not express the meaning of the English sentence. Left hand is that there exists c which is not in South America after moving $\neg$ inside the sentence, which considers country out of South America and is definitely wrong.

(iv) (2) is syntactically invalid and therefore meaningless. '=>' signal can't be used like that with such logic.



### e.

(i) (1) correctly expresses the English sentence. Extract $\neg$ outside and we will get that for every x,y x is a country and y is a country and x,y border and MapColor(x) equals MapColor(y) is false, which represents same meaning as No two adjacent countries have the same map color.

(ii) (1) correctly expresses the English sentence. It's also true but Borders() function will guarantee that x is not equals y otherwise they don't border.

(iii)  (3) is syntactically valid but does not express the meaning of the English sentence. It means that all x,y are countries and x,y border and they have different map color, which is definitely different from original meaning.

(iv)  (2) is syntactically invalid and therefore meaningless. Invalid use of MapColor() function.



## Q3.

### a.

Suppose that X represent which coin we drew, the Bayesian network is as below :

​	![image-20201219014240081](C:\Users\THINKPAD\AppData\Roaming\Typora\typora-user-images\image-20201219014240081.png)

​															Figure.4 Bayesian network

​	

### b.

We can calculate a,b and c's probability for 2 heads and 1 tail.

P(a|2 head 1 tail) = P(a & 2 head 1 tail) / P(2 head 1 tail) = P(a & 2 head 1 tail) / [P(a & 2 head 1 tail)+P(b & 2 head 1 tail)+P(c & 2 head 1 tail)] 

Since P(a & 2 head 1 tail) = 1/3 *( $C_{3}^{1}$ *(1 - 0.2) *$C_{3}^{2}$ * $0.2^2$ ) = 0.096,

P(b & 2 head 1 tail) = 1/3 * ( $C_{3}^{1}$ *(1 - 0.6) *$C_{3}^{2}$ * $0.6^2$ )  = 0.432,

P(c & 2 head 1 tail) = 1/3 *  ( $C_{3}^{1}$ *(1 - 0.8) *$C_{3}^{2}$ * $0.8^2$ )  = 0.128,

so P(a|2 head 1 tail) = 0.096/(0.096+0.432+0.128), P(b|2 head 1 tail) = 0.432/(0.096+0.432+0.128), P(a|2 head 1 tail) = 0.128/(0.096+0.432+0.128).

It's clear that  P(b|2 head 1 tail) is the biggest with the same denominator. Thus coin b is more likely to have been drawn from the bag.

   

