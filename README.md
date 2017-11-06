20171102:
1.rcnn-sppnet-fastrcnn-fasterrcnn 
2.rcnn系列和ssd、yolo的不同
3.比如过拟合怎么办这个问题，第一种你回答了drop out，data augmentation ， weight decay。面试官就觉得你还不错了，但是第二种会接着这个问题，如果你讲了weight decay，立马问你常用的weight decay有哪些？怎么处理weight decay的权重。如果你讲了L1，L2。让你比较为什么要两种weight decay，区别在哪里。比如如果你讲L1零点不可导才用L2，那么立马问你SMOOTHL1。如果你都说明白了，就问你为什么weight decay能够一定程度解决过拟合？如果你说到了L0和稀疏性。接着就来问你为什么稀疏性有效？最后很可能面试官会挖到，如无必要勿增实体的信念问题。但当然不能首先就讲哲学层面，个人觉得工科生一定要由果推因。

作者：匿名用户
链接：https://www.zhihu.com/question/41233373/answer/154948147
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

正则项问题，搞清楚（适合什么样的数据，为什么fast rcnn里写了这样一句话"...... L1 loss that is less sensitive to outliers than the L2 loss used in R-CNN and SPPnet."）

4.lstm和rnn
作者：匿名用户
链接：https://www.zhihu.com/question/41233373/answer/154948147
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

同样，让你对比新旧方案，比如有大部分人觉得基本RNN就是没有LSTM好，这么直接的答肯定不对的。就比如首先问你觉得LSTM解决RNN的梯度消失问题了吗？这个回答要针对LSTM版本以及看面试官想听哪种，笼统来说，如果你回答很大程度解决了，接着就问如何解决的。如果你回答CEC的vanilla版本的LSTM通过加法修正而不同于RNN连乘。那么面试官追问遗忘门是不是连乘，是否带来梯度消失？如果面试官问到这一步，你肯定要修正答案了，现在回答应该是：带遗忘门的LSTM没有本质解决RNN的梯度消失，这个时候你再对LSTM和RNN进行优劣分析就知道LSTM实际上不同于RNN，后者把信息分配与‘过往’如何对当下造成影响都用一个W权重表示。而LSTM则通过遗忘门Wf专注把信息trap进来，仍通过另一个Wi去表示‘过往’对当下造成的影响。很显然这里RNN就少用了一部分权重来建模这个问题。如果要解决的问题中用LSTM解决，遗忘门训练出来的理想状态是失效（全部忘记）的话，那么RNN方法肯定要优于LSTM的。包括对比DL方法和传统ML方法。一定要深谙两种方法具体特点才能答出各自优劣，最终面试官很可能在考验你有没有‘天下没有免费的午餐’这种思想。

5.这个问题被问到过
用贝叶斯机率说明Dropout的原理Dropout as a Bayesian Approximation: Insights and Applications
何为共线性, 跟过拟合有啥关联?Multicollinearity－Wikipedia共线性：多变量线性回归中，变量之间由于存在高度相关关系而使回归估计不准确。共线性会造成冗余，导致过拟合。解决方法：排除变量的相关性／加入权重正则。

作者：许韩
链接：https://www.zhihu.com/question/41233373/answer/145404190
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

6 无偏估计
https://www.zhihu.com/question/38185998

