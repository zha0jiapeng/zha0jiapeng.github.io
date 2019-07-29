# 面试题
## 前言
今天去面试发现有很多之前面试过的题，如今不整理都不记得了,今天决定把所有遇到的面试题和最优解记录再这里。(持续更新)
### java基础相关
1. List list = new ArrayList(20)扩容了几次?
   > 这是ArrayList传入构造器
   ```
        transient Object[] elementData;
        
        public ArrayList(int initialCapacity) {
        if (initialCapacity > 0) {
            //这里会初始化数组的长度重新赋值给Arraylist初始化的数组
            this.elementData = new Object[initialCapacity];
        } else if (initialCapacity == 0) {
            //传0的话 跟没传没区别
            this.elementData = EMPTY_ELEMENTDATA;
        } else {
            throw new IllegalArgumentException("Illegal Capacity: "+
                                               initialCapacity);
        }
    }
    ```
    >得出结论 根本没扩容
   
    


