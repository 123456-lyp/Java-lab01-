# 一、实验目的
1. 基本掌握IntelliJ IDEA Community Edition的使用方法
2. 掌握Java源程序命名、运行方法
3. 理解、掌握创建包的方法
4. 初步了解类的实例化方法
# 二、实验要求
1. 定义包
2. 组织类
3. 定义类的属性、方法
# 三、解题思路
### **步骤一**：
&emsp;&emsp;**根据老师所给的部分源文件，通过阅读理解其中代码所代表内容，基于三个源程序之间的关系，文件分别描述了银行账户、存款人员、测试类。设计了本次实验程序。**
<br><br>&emsp;&emsp;以下三个java源程序文件首先是存在在同一个包里，这就意味着他们是共同处理同一个事件的。三个源文件分别放置了不同类，其中两个类是代表两个不同种类的事物，第三个是一个含有主函数的测试类，主要作用是用来测试前两个类中方法是否能够正常使用。
### **步骤二**：
&emsp;&emsp;**配置环境，在所配置的环境内搭建逻辑关系，分别代入三个源代码。**
### **步骤三**：
&emsp;&emsp;**在Customer类中新添加一个属性age，描述其年龄，并补充操作年龄的方法getAge。在测试类中调用这些方法。**
### **步骤四**：
&emsp;&emsp;**在前期准备工作完成后，准备在理解的基础上复写程序。**

# 四、流程图

![avatar](https://github.com/Minomeis/Experiment01/blob/master/img/liucheng.jpg)
# 五、关键代码
1. Account类里面，有两个函数用来实现存钱和取钱。通过布尔类型，来判断取钱的金额是否是这个账户能负担得起的。
```java 
    public double getBalance(){
        return balance;
    }
    public boolean deposit(double amount){
        balance=balance+amount;
        return true;
    }
    public boolean withdraw(double amount){
        boolean result=true;
        if(balance<amount){
            result=false;
        }
        else{
            balance=balance-amount;
        }
        return result;
    }
```
2. Customer类里面，添加age属性，与构造函数的参数相对应。
```
private int age;
```
3. TestBanking类里，采用如下方式，将Account和Customer实例化，并将两者联系在一起。
 ```
    Customer customer;
    Account account;
    customer.setAccount(new Account(500.00));
    account=customer.getAccount();
 ```

# 六、系统运行截图
&emsp;&emsp;下图是本实验主程序TestBanking.java的运行结果。
![avatar](https://github.com/Minomeis/Experiment01/blob/master/img/001.jpg)

# 七、感想与体会
&emsp;&emsp;通过本次实验，让我感受到了“万事开头难”这个道理。就这个实验总体来说并不算困难。但是安装idea的过程比较艰辛。在这上面，虽然看似简单，但是确实也是花费了不少功夫。老师给的教程可能并不是很适用，因此，还需要自己花费时间去查找资料，并且克服各种问题，安装成功。
<br>&emsp;&emsp;对于后续的程序阅读来讲，对于成绩一般的我来说也比较困难，我一行一行仔细阅读，当遇到读不懂的和很吃力的地方，就积极的到网站上去查找并解决问题。但是还是会有很多小细节没有理解透彻。
<br>&emsp;&emsp;对于整体的实验过程来讲让我收获了很多。从代码上来说，让我更好的了解了文件的整体结构形式。同时，还学会了新的用法，比如boolean类型，是之前没有接触过的，通过自己学习明白了大致。
<br>&emsp;&emsp;最后就是在学习方法上，需要我自己充足的主动性。不仅要上课认真，同时也要多加查询资料自学，能够很大的提升我对专有名词的熟悉程度，对于我理解代码也有很大的帮助。希望我自己对Java有更深入的理解，更灵活的应用。
