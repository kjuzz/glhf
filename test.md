# lecture 1: What is computation?
1.python中一切都是object，python程序对这些object进行操作，object一定会有type。 基本数据结构int是object, 由基本数据结构组成的class也是object, 这些数据结构和class的实例也是object。type(int) type(5)
2.int, float, bool, NoneType.
3.type convert 类型转换 int(1.2) float(2)
a=1, b=2, c=a+b, print(c), a+=1, print(c)
# pset0:
Anaconda是一个科学计算环境，当在电脑上安装好Anaconda以后，就相当于安装好了Python，这里面还有一些常用的库，如numpy，scrip，matplotlib等库。如果你这里没有安装anaconda的话，直接安装了Python，装完Python 想要使用这些库的话 还要在cmd中运行 pip install ...;，就是需要自己不断地添加库。而Anaconda下里面就有许多常用的库，可以直接使用，方便快捷。
spyder就是ide。
input的用法：num = int(input("Type a number... "))
log的用法：import numpy, numpy.log(2)
# lecture 2: Branching and Iteration
比较算符和逻辑算符
for 和 while 循环区别： while循环有时并不能改写成for循环。
range(start, stop, step)
break
lecture 3: String Manipulation, Guess and Check, Approximations, Bisection
strings: s = "abcdefgh", s[3:6], s[3:6:2], s[::-1], s[4:1:-2]
guess and check: 求立方根：1.顺序猜 2.二分猜 两者区别在于第一个你的区间step要设置为精度要求，二分猜则要一直分到满足精度为止。完美立方根
求一个数的立方根，误差不超过0.01.
数据结构 控制流 和erro

int, float
数据结构的相
string 在python中可以改变吗? c/c++中呢? 在内存中是如何储存的呢?
list
alias,cloning的区别？
.append，.extend，del(), +, .remove, .pop, list(), .split(s), ' '.join(L), .sort(), .reverse(), sorted(), sorted(    , reverse = True)
.sort()有返回值吗？sorted()呢
l=l.append() l是什么? 
L1 = ["bacon", "eggs"] b=L1 L1=["gg"] print(b)
sentence.strip()，sentence.replace(" ", "")，string.split(), " ".join(sentence.split())
remove 和 del的区别del是从下标入手，而remove是从值入手
list和string的互相转化list和join
sorted() 和l.sort()
tuple
(1,)和(1)的区别? [1]和[1,]呢

set
len(set('aabbcd'))
图论 
节点和边都是类，然后digraph也是一个类，先输入节点，再输入边，主体是一个dic，一个节点对应一个list，这个list中放该点链接的点
graph是digraph上的一个新类，更改了dig中的addedge函数。
最短路径dfs，要有一个path表示当前路径, 第一次找到终点的时候才会输出一个最短路径, 此前的输出一直是none, 当shortest存在的时候, 每次都输出一个最优的. 结构上用for然后不断的递归, 就可以做到dfs
bfs, 一个经典的做法就是一个queue, 这个queue里面放要处理的路径, 不断的在这个queue中append新的元素(当没有遇到终点, 就一直append, 遇到终点,此时一定是最短路径)

问题和算法 什么是算法?
猜测型
平方根问题:
顺序猜测
二分猜测
均值猜测
如何确定一个数是否是perfect平方根？
公式型
解方程
递归
dynamic programing

数据结构和object的区别？

底层
计算机和计算器的区别?
基本指令和指令集 move left, move right, read, write, scan, and do nothing

逻辑运算有哪些？比较运算呢？这些运算的结果是什么？
数学运算 a//b，math.sqrt(a)，math.log(100,10), //, %
控制流for while break
输入输出
range 和 index s="abcdef"这里最大的index是几？len(s)是几？s[0:maxindex:1]和s[0:len(s):1]的区别
in range()
That's because 0.1+0.1+0.1 is not equal to 0.3. 0.1 cannot be precisely represented as a floating point number, so 0.1+0.1+0.1 = 0.30000000000000004. When you are trying to take simple counts of elements, always use integers to avoid this type of problem.
不要写全局变量

根据买房软件的推算，在美国买房子还是在中国买要取决于倍数关系，房价是多少倍，工资是多少倍？

什么是数学归纳法？什么是递归？inductive

乘法；阶乘？前面两个如何用非递归？；什么是汉诺塔，其递归是什么样子？；什么是fibonacci数？对fn进行解释；如何判断string是否是回文?

list.index，找到学生成绩的办法
什么是dictionary？在p中如何实现？如何初始化？，key，value分别是什么？test，add，del？keys，values，iterables是什么？keys的要求？
+
.
如何统计频率？如何根绝最大频率找到相应的key？如何将strings变为小写且除去空格？如何trim？对于这个统计歌词中单词的频率例子，如何让找到某个频率以上所有的单词，并标出它们的频率？strip, split, join

d.keys()的类型是什么？class dict_keys

for k in dict:
        if dict[k] == best:

testcase？写完一段之后，确保自己写的代码做出正确的事情可以吗？glassy box？black box？备份？

try: a = int(input("Tell me one number:")) b = int(input("Tell me another number:")) print(a/b) except: print("Bug in user input.") 解释try和except的作用

try: a = int(input("Tell me one number: ")) b = int(input("Tell me another number: ")) print("a/b = ", a/b) print("a+b = ", a+b) except ValueError: print("Could not convert to a number.") except ZeroDivisionError: print("Can't divide by zero") except: print("Something went very wrong.")解释这些except

为什么发生错误的时候返回一个值不好？什么是好的办法？

SyntaxError， TypeError， NameError， NameError

try except，raise，assertion的区别？
def get_ratios(L1, L2):
    """ Assumes: L1 and L2 are lists of equal length of numbers
        Returns: a list containing L1[i]/L2[i] """
    ratios = []
    for index in range(len(L1)):
        try:
            ratios.append(L1[index]/L2[index])
        except ZeroDivisionError:
            ratios.append(float('nan')) #nan = Not a Number
        except:
            raise ValueError('get_ratios called with bad arg')
        else:
            print("success")
        finally:
            print("executed no matter what!")
    return ratios

def avg(grades):
    try:
        return sum(grades)/len(grades)
    except ZeroDivisionError:
        print('warning: no grades data')
        return 0.0

avg function: version with assert
def avg(grades):
    assert len(grades) != 0, 'warning: no grades data'
    return sum(grades)/len(grades)

什么是hangman？如何实现？总的字母集合，猜到的字母集合，猜过的字母集合，是否猜到
def load_words():
    inFile = open(WORDLIST_FILENAME, 'r')
    line = inFile.readline()
    wordlist = line.split()
    print("  ", len(wordlist), "words loaded.")
    return wordlist
wordlist = load_words()

def choose_word(wordlist):
    return random.choice(wordlist)
secret_word = choose_word(wordlist)
hangman_with_hints(secret_word)

判断某一个数是否为质数，为什么到i//2就行？如何用标志位？如果是直接跳出呢？
筛选法判断素数是什么意思？

如何做一个testcase
def test_get_word_score():
    """
    Unit test for get_word_score
    """
    failure=False
    # dictionary of words and scores
    words = {("", 7):0, ("it", 7):2, ("was", 7):54, ("weed", 6):176,
             ("scored", 7):351, ("WaYbILl", 7):735, ("Outgnaw", 7):539,
             ("fork", 7):209, ("FORK", 4):308}
    for (word, n) in words.keys():
        score = get_word_score(word, n)
        if score != words[(word, n)]:
            print("FAILURE: test_get_word_score()")
            print("\tExpected", words[(word, n)], "points but got '" +
                  str(score) + "' for word '" + word + "', n=" + str(n))
            failure=True
    if not failure:
        print("SUCCESS: test_get_word_score()")

Notice how the repeated letter 'l' is represented. With a dictionary representation, the usual way to access a value is hand['a'], where 'a' is the key we want to find. However, this only works if the key is in the dictionary; otherwise, we get a KeyError. To avoid this, we can instead use the function call hand.get('a',0). This is the "safe" way to access a value if we are not sure the key is in the dictionary. d.get(key,default) returns the value for key if key is in the dictionary d, else it returns default. If default is not given, it returns None, so that this method never raises a KeyError.

num_vowels = int(math.ceil(n / 3))
handCopy = handOrig.copy()

EVERYTHING IN PYTHON IS AN OBJECT (and has a type)，object是一种class。python在object宇宙中。

class student（ob）：
    def init（self，number，grade1, grade2 ）:
            ...
    def str (self)
    def ave(self, grade1, grade2)
为什么get_age要比.age要好？为什么直接访问attributes不好？

default arguments？over write str?

class variables?

Some people tried to store Position objects in their data structure of clean tiles 
def isTileCleaned(self, m, n): 
newPosition = Position(m, n) 
return newPosition in self.cleanTileList
the default way Python checks if they are equal is to check the location where that object is stored in memory. Because this code creates a new Position object, newPosition, it makes sense that this particular instance being created is not stored in the same location as any other Position object in the list of clean tiles! Therefore, of course it won't be found when Python checks to see if it's in the list. There are a couple of ways to avoid this issue. Our recommended way for the purposes of this course involves changing what is being stored in the data structure. Representing a set of x, y coordinates as a tuple would make testing for equality much simpler.
用position对象做一个list记录哪些瓷砖被清理过，对position（m，n）而言有一个判断是否清理过的函数，这里的意思是新造一个mnposition判断是否在list中，这样子是不可行的，你会有两个mn'position，一个在list中一个不在list中，推荐的做法是用在list中放tuples

用递归的时候的思想

关于引用函数

贪心算法，surveillance监视，quadratic二次的，heterogeneous合成的， polynomial多项式
O，最坏情况的上界
二分搜索，在一个已经排好序的list中，坏的情况是logn，其他情况不到logn。但是在L[:half]， L[half:]的情况下由于会复制list
二叉搜索
i是int，digits[i%10循环]的复杂度，汉诺塔的时间复杂度。
找子集power set的算法和时间复杂度
l[:-1]，l[-1:]
非递归的feb写法，递归写法，他们的时间复杂。

查找和排序，首先对于未排序的只能遍历查找。
如果对于已经排好序的可以遍历也可以二分，如果用遍历虽然时间复杂度是n但是实际会小于这个，因为当你找到比要找的数大的时候就可以停止了；如果用用二分查找logn

c语言
源文件采用什么编码? 编码字符集和运行字符集有什么区别? 十进制和二进制之间如何转换?  ASC, GBK, Unicode 分别是什么?
编译是什么? 链接呢? 编译出来的二进制文件为什么不可以直接运行呢? 如何编译呢? 
整数是如何储存的? 浮点数是怎么储存的?源代码是如何储存的? 如何将源代码编译成目标文件? 
什么是缓冲区/缓存? 如何读写硬件呢? 
二维数组的操作?  如何求数组的长度? 
什么是预处理? 这个行为是在什么之前? 其对象是什么? 什么是宏? 什么是带参数的宏定义? 什么是条件编译? #和##的用法? 有哪些预定义宏?  #define SQ(y) ((y)(y)) SQ(i++) * LINE：表示当前源代码的行号；FILE：表示当前源文件的名称；DATE：表示当前的编译日期；TIME：表示当前的编译时间; STDC：当要求程序严格遵循ANSI C标准时该标识被赋值为1；__cplusplus：当编写C++程序时该标识符被定义
你写的程序运行时如何操作硬件? 不同的操作系统会对此有影响吗? 
指针, 什么是二级指针? 什么是未赋值指针和 空指针? void 和void的区别? 为什么需要类型转换?

算法问题
如何解决最优化问题? 贪心或者硬来
硬来的思路是什么? 从切杆和找食物的问题来分析. 对于找食物的话, 就是取这个食物和不取这个食物两种情况取较大的值, 对于切杆问题的话也是找最大值. 两个问题本质上一样的, 
什么是dynamic pro? 什么是相同的节点?
贪心, 什么是01背包问题? 什么是选择的食物? 分别用贪心算法?用全集的方法呢? 两个的复杂度分别是多少? n个元素的全集是多少? 什么是备忘? 什么是时空权衡? 如何编码可以压缩存储空间? 你有多少种编码方式? 变长编码的基本思想? 什么是铁头流编码? 什么是哈夫曼算法?它实现了什么?  为什么哈夫曼编码可以带来最少空间? c++和python怎么实现哈夫曼编码? 从下往上和从上往下? ]什么是活动选择问题?  对最早结束时间的思路需要给出两种算法. 
数制和编码, 如何数制转换? 等长编码和变长编码分别是什么? 两者有什么区别 ? 循环码是哪一种? 什么是码表? 什么是奇偶校验码? 什么是字符码?

动态规划, 就fib函数而言, 动态规划实际上是将要计算的树变窄了. 就作业中的金鸡蛋问题, 实际上是比较f(选择1, lim-x) 和f(不选1, lim)的大小的问题. 对于这里这个问题, 只要剩余重量一样, 就是一个重复的问题. 鸡蛋问题中, 要求的是最少的鸡蛋数量.
对于切杆子的问题, 从0-n, 0为最大值, 然后不断更新, 看有没有比这个值更大的.
对于鸡蛋问题也是这个思路, 在所有情况中找最小值.

用计算机仿真掷硬币的过程, 仿真得出得到某种特定结果的频率. 需要知道目标结果, 需要知道试验次数. 十万次的仿真结果小数点第一位是一样的. 不过这是小概率事件的仿真.

一年有366天, 每天是生日的概率相同, 367个人, 至少有两个人生日相同的概率是多少? 
如何仿真? 每个人都是在366天中随机选一个作为生日, 最后看生日相同人数数量是否大于2. 这是一个样本. 如果组里有37个人的话, 那么这个事件是必然发生的. 如果有366 个人, 至少有两个人生日相同的反面是所有人的生日都不相同, 如果有366个人的话这个事件还是有可能发生的, 比较好确定概率, 概率十分小. 
如果组里的人数是n, 这个问题的反面还是比较好确定, 就是n个人的生日都不相同. 两个人不相同的概率是366365/366366, 这是一个大概率事件, 随着人数增长, 分子的增速和分母的增速逐渐变化, 最后导致结果变化.

图论
结构和初始化
两个重要的成分是边和节点, 在py的世界中, class node应该包括该点的名字, class edge 应该包括该边的起始点和终点.
通过这两个结构, 我们可以实现digraph, 核心是一个邻接矩阵, 实际上是一个dic, 一开始是一个空的, 然后不断addnode和addedge这个矩阵如何实现, 初始化一个dic, 所有的节点都应该成为keys, 然后对应的每一个value是一个链表, 储存所有和它相邻的节点. 
graph是一种digraph之上的结构, 它的addedge引用了两次第digraph的addedge
在这里注意, 如果一个图的结点只有123, 但是他的边却涉及到4, 那么我们有矛盾.另外 节点有可能没有被边连接, 这就是为什么既要有节点, 也要有边的原因.
前面的三个都是结构, 建一个图的话你需要g=digraph() 这是一个空的图, 然后你需要g.addnode 以及 g.addedge. 实际上将一个结构变成实体, 就是将结构的属性赋予值, 比如digraph这个结构只有一个属性, 然后你需要将这个属性初始化, addnnode(node("hefei")) 里面这个node("hefei")实际上是初始了一个叫hefei的node, node结构只有一个属性叫做名字. addedge()函数里面要是一个edge结构, edge((g.getNode('Boston'), g.getNode('Providence'))就可以初始化一个edge实体
最短路径问题
为什么dfs可以用里找最短路径?

面向对象的编程 和一般函数 的区别, 面向对象编程的你可以看出来一个对象中 所有的东西, 如果其中某个函数是别的对象也会用到你可以 在两个对象 下再设立一层. 所有的对象一开始都是从object这一对象开始继承
assertEqual(str(self.g), expected)
indent/ rig/ coherent/ lid / moth/ propogating/ populate
swap /(x,y)=(y,x) 这是tuple
关于list

assert len(grades) != 0, 'no grades data' 防止进入未知领域

如何建立一个graph, 首先需要node 和 edge class, node的属性只有其名称, edge的属性是其起点和终点, 这两个点都是node这个class的. 然后class digraph的属性是一个字典, 方法是add node 和add edge. 初始化这个的时候先得到一个字典是空的实例. graph 和digraph是不一样的, graph要在digraph的基础上实现, 因为两次用到digraph中的addedge

dfs
电路, 信号, 模电, 数电
