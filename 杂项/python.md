# Here  I will record my process of learning of python
##   **的用法 
#### \*\*类似于^幂运算  例如 3**2 = 9<br>
#### 但是需要注意的是在python优先级中 需要注意幂运算的优先级  例如 -3**2 = -9  ,如果需要得到想要的结果 ,则需改变成 (-3)**2   而 3**-2 与 3**(-2)的结果是一样的 ,<br>即 `幂运算中负号的优先级一般右侧要比左侧的高`
## for循环的用法
### 语法:
```Python
for 目标 in 表达式 :
	循环体
```
### for经常与range()一起使用
```Python
	for i in range(5):
		print(i)
0 1 2 3 4
```
```Python
range(2,9)

2 3 4 5 6 7 8  #注意这里没有9
```
```Python
range(2,9,2)
2 4 6 8  #第三个参数类似于 i=i+2
```
## 列表
### 在python中,列表类似于C的数组,却更像是打了激素的数组,
<br>例如
```Python
mix =[1,2,'123',[1,2,3]]
```
## 给列表中添加元素的方法
1.append()  
```Python
mix.append("李梦洋")	#append每次只能加`一个元素`进入到列表中去
```
2.extend()
```Python
mix.extend(["12","133"])	#extend每次只能加入一个列表进入到列表中去,即extend的参数只能是一个`列表`
```
`注意:append 和 extend 两个方法都是将元素添加到列表的最后位置`
3.insert()
```Python
mix.insert(0,"123") #第一个参数表示添加元素在列表中的位置,第二个参数表示添加的元素
```
## 从列表中获取元素
```Python
mix[0]
```
## 从列表中删除元素
1.remove()
```Python
mix.remove("李梦洋")  #不需要知道元素在列表中的位置
```
2.del  ` del 不是函数 `
```Python
del mix[0]  #删除第0个元素
del mix 	#删除整个列表
```
3.pop  
```Python
mix.pop()	#删除并返回列表中的最后一个元素,与 堆栈的原理相同
mix.pop(i) 	#参数表示删除并放回列表中的第i+1个元素
```
## 列表分片  slice
```Python
mix[1:3]   #返回值为 mix[1] 和mix[2] ,不包含mix[3],同时不会改变源列表
mix[x:y]	#x和y参数可以省略  如果x y都省略,则表示列出列表中所有的元素 与 mix含义相同
```
## 列表的对比
列表可以直接进行比较,当列表中的元素较多时,比较两个列表的首元素大小,如果两个元素首元素相同,再比较次元素的大小,以此类推
## 列表中元素的处理

1.count()函数
```Python
mix.count(x)  #求x在列表mix中出现的次数 
```
2.index()函数
```Python
mix.index(x)  #求x在列表mix中第一次出现的位置
mix.index(x,y,z)	#求x在列表mix中 y到z区间第一次出现的位置 其中z 可以省略
```
3.reverse()函数
```Python
mix.reverse() 	#使mix列表原地反转,第一个变成倒数第一 ,倒数第一变成第一
```
4.sort()函数
```Python
mix.sort() 	使mix列表的元素从小到大排列
mix.sort(reverse = True )  	使元素从大到小排列
```
5.拷贝
```Python
mix1 =mix[:] 	#若采用分片方法,mix1不会跟着mix改变而改变  即mix1另外重新分配了内存地址
mix1=mix   	#这种方法导致mix1 会跟着mix改变而改变   即mix和mix1 都指向同一内存地址
