# 第一周  
## 1 机器学习是什么？（定义）
1. *Arthur Samuel*：他定义机器学习为，在进行特定编程的情况下，给予计算机学习能力的领域。
2. *Tom Mitchell*：一个程序被认为能从经验E中学习，解决任务T，达到性能度量值P，当且仅当，有了经验E后，经过P评判，程序在处理T时的性能有所提升。（人话：经验E 就是程序上万次的自我练习的经验而任务T 就是下棋。性能度量值P呢，就是它在与一些新的对手比赛时，赢得比赛的概率。）
## 2 监督学习和无监督学习
### 2.1监督学习  
#### 2.1.1例子
* 例子1-卖房子
  * 数据：横轴表示房子的面积，单位是平方英尺，纵轴表示房价，单位是千美元。
  * 问题：假如你有一个朋友，他有一套750平方英尺房子，现在他希望把房子卖掉，他想知道这房子能卖多少钱。
  * 算法：可以在这组数据中画一条直线，或者换句话说，拟合一条直线，根据这条线我们可以推测出，这套房子可能卖＄150,000。用二次方程去拟合可能效果会更好。根据二次方程的曲线，我们可以从这个点推测出，这套房子能卖接近＄200,000。
* 例子2-查肿瘤
  * 数据：横轴表示肿瘤的大小，纵轴上，我标出1和0表示是或者不是恶性肿瘤。我们之前见过的肿瘤，如果是恶性则记为1，不是恶性，或者说良性记为0。
  * 问题：我有5个良性肿瘤样本，在1的位置有5个恶性肿瘤样本。现在我们有一个朋友很不幸检查出乳腺肿瘤。假设说她的肿瘤大概这么大，那么机器学习的问题就在于，你能否估算出肿瘤是恶性的或是良性的概率。用术语来讲，这是一个**分类问题**。
#### 2.1.2回归和分类
* 回归问题(regression)-对应例子1
  * 在房价的例子中，我们给了一系列房子的数据，我们给定数据集中每个样本的正确价格，即它们实际的售价然后运用学习算法，算出更多的正确答案。比如你朋友那个新房子的价格。我们**试着推测出一个连续值的结果**，即房子的价格。
  * 一般房子的价格会记到美分，所以房价实际上是一系列离散的值，但是我们通常又把房价看成实数，看成是标量，所以又把它看成一个连续的数值。
  * 回归这个词的意思是，我们在**试着推测出这一系列连续值属性**。
* 分类问题（classification）-对应例子2
  * 分类指的是，我们**试着推测出离散的输出值**：0或1良性或恶性，而事实上在分类问题中，输出可能不止两个值。比如说可能有三种乳腺癌，所以你希望预测离散输出0、1、2、3。0 代表良性，1 表示第1类乳腺癌，2表示第2类癌症，3表示第3类，但这也是分类问题。
  * 分类即是**推测出离散值**，分类问题目标是**推出一组离散的结果**。
* **简单来说：回归问题-预测连续值；分类问题-预测离散值。**
#### 2.1.3基本思想
**我们数据集中的每个样本都有相应的“正确答案”，再根据这些样本作出预测**，就像房子和肿瘤的例子中做的那样。
### 2.2无监督学习

### 2.3区别
1. 