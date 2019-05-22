
>公司规模：499-999
要上市


###### 一面 、
- java的内存区域有哪些（回答了jvm书上的那几块）
- jvm为啥设计栈这个数据结构（本人从方法的调用会产生帧栈来回答了一下。又说方便调用。面试官也很好又补充了一点）
- 垃圾回收 （问了那些搜索收算法，那些回收算法，就说了些名词 应届没问内深）
- 说说view事件体系（开发艺术书上的view那几节的目录章节说了下）
- 说说view事件的分发机制（简单说下分发流程  答案如下伪代码）

```java
public boolean dispatchTouchEvent(MotionEvent ev) {
        boolean consume = false;//事件是否被消费
        if (onInterceptTouchEvent(ev)){//调用onInterceptTouchEvent判断是否拦截事件
            consume = onTouchEvent(ev);//如果拦截则调用自身的onTouchEvent方法
        }else{
            consume = child.dispatchTouchEvent(ev);//不拦截调用子View的dispatchTouchEvent方法
        }
        return consume;//返回值表示事件是否被消费，true事件终止，false调用父View的onTouchEvent方法
    }

onTouchEvent（MotionEvent ev）{
   if(消费){
   
     判断，进行 消费处理
     
   }else{// 不消费时
      super.onTouchEvent(ev)
   }
}

```
参考：
(View的事件体系（三）view的事件分发机制)[https://blog.csdn.net/qq_38350635/article/details/89158550]
- handler 机制（感觉应届必须掌握。回答了主要用来更新ui，handler相关类MessageQueue介绍，相关类Loop介绍。）
- 平时使用handler时loop在哪初始化的
- messagequeue 、handler、loop 三者如何工作（简单说了下子线程发送消息到消息队列，loop不停轮询取出 交给 handler的 handlerMessage处理。还好没深入问了，应届的渣渣不能再装逼了）
- loop取消息是怎样循环的（记得以前看过好像是for（；；）答了死循环，又问为啥没有阻塞主线程，这个以前见过 没有深入了解就如实交代了。。。。。）
- ipc 方式有哪些（开发艺术有  随便bb了四五种）
- okhttp、glide、这些使用到了啥程度（源码没研究过，会简单封装okhttp+Gson，看着开发艺术仿写过ImageLoader）
- 你有啥问我的（随便问了几句）

> 等着我去叫总监

###### 二面、
- 上家公司实习干了啥（说了下）
- 应用商店看了下上家公司的app（我没安装哈）
- 能接受加班不我们公司要上市今年开始早10晚9，可以提前走 一般都是九点走。（感觉公司还行 答应能接受）
- 总监开始说加班的好处（能学到很多，之类的）
- 介绍公司平台大
- 哪里人？（回答河南的 一听第一个面试我的那哥们是我老乡）
>等着我去交hr

###### 三面、 

hr小姐姐
- 问薪资  要了9.7（先提个高的 上家打算给的）
- 吹泡泡（对996的看法，三年规划努力提生自己 。。。。 打压下你）
- 高学历的应届生 心浮不能静下心工作，天天想着跳槽（自己感觉二本的我学历渣渣啊，继续打压）
- 又吹了一会总监合工大毕业很厉害（我堂弟保研哈工大我内心嘀咕了句）
- 最低要求多少（昨天面了一家开8-9之间，就说了8-9吧不能比实习的那家应届开的差太多啊）
- 好了争取帮你9
- 住哪之类的（想让我住公司近点。。。。。难受啊马飞飞，还是想让加班）
- 下周一能报道吗（可以，随时到岗。。。。）

就想起了这么多、、、、、、

>回去互换了微信 hr说 薪资ok了 正在申请职位。。。。。应该稳了
应届第一份工作 好好干了。。。。。。溜




