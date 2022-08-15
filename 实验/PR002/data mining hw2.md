# data mining hw2

2019K8009907018 王畅路

## 1.

|      | Height | Hair  | Eye   | Class |
| ---- | ------ | ----- | ----- | ----- |
| 1    | Tall   | Blond | Brown | C1    |
| 2    | Tall   | Dark  | Blue  | C1    |
| 3    | Tall   | Dark  | Brown | C1    |
| 4    | Short  | Dark  | Blue  | C1    |
| 5    | Short  | Blond | Brown | C1    |
| 6    | Tall   | Red   | Blue  | C2    |
| 7    | Tall   | Blond | Blue  | C2    |
| 8    | Short  | Blond | Blue  | C2    |
| 9    | Medium | Dark  | Blue  | C2    |

（a）Compute the information gain for height,hair,eye.



For the whole class C:

$H(C) = -\frac{4}{9}log_2\frac{4}{9} - \frac{5}{9}log_2\frac{5}{9}$

For height:

$g(C,height) = H(C) - H(C|height) = 0.14556045156746533$

For Hair:

$g(C,hair) = H(C)-H(C|hair) = 0.1860635600786077$

For Eye:

$g(C,eye) = H(C)-H(C|eye)= 0.3788788371352292$

（b）Construct a decision tree with information gain



according to a,let us use Eye as the first classification

after that the brown eye are all C1, there is no need to classify them

then after calculating the information gain we choose Hair as the next classification.

repeat as above,we generate a decision tree as follow.

<img src="C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20220509085813470.png" alt="image-20220509085813470" style="zoom:67%;" />

## 2.

(a)

suppose X is students, Y is  the identity of the student

$P(Y = graduate|X=smokes)=\frac{P(X=smokes|Y=graduate)P(Y=graduate)}{P{(X=smokes)}} =\frac{0.23*0.2}{0.2*0.23+0.8*0.15}=27.7\%$

(b)

more likely to a undergraduate student.

(c)

suppose U is living in a dorm or not,because smoke and living in a dorm is independent

$P(Y = graduate|X = smokes,U = living) = \frac{P(X=smokes|Y=graduate)P(U = living|Y=graduate)P(Y=graduate)}{P(X=smokes)P(U=living)}=59.4\%$

## 3.



<img src="C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20220509110827218.png" alt="image-20220509110827218" style="zoom:67%;" />

given a instance(T,T,1,1)

then a1 = T,a2 = T,normalize a3, a3 = 0

| a1   | a2   | a3   | w1   | w2   | w3   | w4   | w5   | w6   | w7   | w8   | x1   | x2   | x3   | c    |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 1    | 1    | 0    | 0.2  | -0.3 | 0.4  | 0.1  | -0.5 | 0.2  | -0.3 | -0.2 | -0.4 | 0.2  | 0.1  | 1    |

| Unit j | Net input Ij               | Output Oj |
| ------ | -------------------------- | --------- |
| h1     | 1x0.2+1x0.4+0x-0.5-0.4=0.2 | 0.450     |
| h2     | 1x-0.3+1x0.1+0x0.2+0.2=0   | 0.500     |
| c      | 0.450x-0.3+0.500x-0.2+0.1  | 0.537     |

| Unit j | Err j                                   |
| ------ | --------------------------------------- |
| 6      | 0.537（1-0.537）（1-0.537）=0.1151      |
| 5      | 0.500（1-0.500）0.1151（-0.2）= -0.0057 |
| 4      | 0.450（1-0.450）0.1151（-0.3）= -0.0085 |

suppose that learing rate is 0.9

| Weight or bias | New Value                      |
| -------------- | ------------------------------ |
| w8             | -0.3+0.9x0.1151x0.450 = -0.253 |
| w7             | -0.2+0.9x0.1151x0.500 = -0.148 |
| w6             | 0.2+0.9x-0.0085x0 = 0.2        |
| w5             | -0.3+0.9x-0.0057x0 = -0.3      |
| w4             | 0.4+0.9x-0.0085x1 = 0.392      |
| w3             | 0.1+0.9x-0.0057x1 = 0.095      |
| w2             | -0.5+0.9x-0.0085x1 = -0.508    |
| w1             | 0.2+0.9x-0.0057x1 = 0.195      |
| x3             | 0.1+0.9x0.1151 = 0.204         |
| x2             | 0.2+0.9x-0.0057 = 0.195        |
| x1             | -0.4+0.9x-0.0085 = -0.408      |

## 4.

1.

| class | 0    | 1    |
| ----- | ---- | ---- |
| 0     | 981  | 9    |
| 1     | 22   | 21   |

2.

| class | 0    | 1    |
| ----- | ---- | ---- |
| 0     | 979  | 11   |
| 1     | 21   | 22   |

3.

| class | 0    | 1    |
| ----- | ---- | ---- |
| 0     | 957  | 33   |
| 1     | 32   | 11   |

4.

from the confusion matrix we can see that 

the decision tree holds the highest accurate rate of 96.7%

the highest sensitivity is neural network of 51.2% 

the highest specificity is decision tree of 99.1%

the highest precision is decision tree of 97.8%

## 5.

### logistic

the parameters and matrix are shown as follows.

![IMG_256](file:///C:/Users/DELL/AppData/Local/Temp/msohtmlclip1/01/clip_image002.jpg)

| class | 0    | 1    |
| ----- | ---- | ---- |
| 0     | 56   | 7    |
| 1     | 3    | 395  |

### decision tree

the parameters and matrix are shown as follows.

![IMG_256](file:///C:/Users/DELL/AppData/Local/Temp/msohtmlclip1/01/clip_image002.jpg)

| class | 0    | 1    |
| ----- | ---- | ---- |
| 0     | 56   | 7    |
| 1     | 1    | 397  |

### neural network

the parameters and matrix are shown as follows.

![IMG_256](file:///C:/Users/DELL/AppData/Local/Temp/msohtmlclip1/01/clip_image002.jpg)

| class | 0    | 1    |
| ----- | ---- | ---- |
| 0     | 50   | 13   |
| 1     | 6    | 392  |

