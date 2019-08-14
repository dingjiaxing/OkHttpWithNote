# 带中文注释的okhttp源码

## 重点类和方法
1. OkHttpClient: okhttp客户端
2. RealCall：
* getResponseWithInterceptorChain：获取响应
4. Chain: 责任链的接口
5。 RealInterceptChain: Chain的唯一一个实现类
* proceed

## 调用过程
1. OkHttpClient.newCall
2. RealCall.enqueue
3. Dispatcher.enqueue

## 分发器
3. DIspatcher: 分发器，负责请求调配和分发
* enqueue：
## 分发器
1。 线程池：0个核心线程，最大线程数不限，60秒后如果不使用便会释放
* 线程池不会一直缓存线程，可能会出现长时间不使用的情况


## 五大拦截器

### 连接拦截器
1. 重要类和方法
* ConnectInterceptor
* ConnectionPool
* RealConnection
* RequestLine
