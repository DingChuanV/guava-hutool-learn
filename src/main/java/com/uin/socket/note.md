BIO 是同步阻塞通信
NIO 是同步非阻塞通信
AIO 是彻底的异步通信。

有一个经典的举例。烧开水。
假设有这么一个场景，有一排水壶（客户）在烧水。

BIO的做法是，叫一个线程停留在一个水壶那，直到这个水壶烧开，才去处理下一个水壶。
NIO的做法是，叫一个线程不停的循环观察每一个水壶，根据每个水壶当前的状态去处理。
AIO的做法是，每个水壶上装一个开关，当水开了以后会提醒对应的线程去处理。

可以看出AIO是最聪明省力，NIO相对省力，叫一个人就能看所有的壶，BIO最愚蠢，劳动力低下。

简单的描述一下BIO的服务端通信模型：
采用BIO通信模型的服务端，通常由一个独立的Acceptor线程负责监听客户端的连接，它接收到客户端连接请求之后为每个客户端创建一个新的线程进行链路处理
处理完成后，通过输出流返回应答给客户端，线程销毁。即典型的一请求一应答通宵模型。
