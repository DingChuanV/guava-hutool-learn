# 滑动窗口-限流
滑动时间窗口就是把一段时间片分为多个窗口，然后计算对应的时间落在那个窗口上，来对数据统计。
随着时间的流失，最开始的窗口也会失效，但是也会生成新的窗口。

交易的频次  2次/s
时间窗口就是 1s, 将 1s 的时间区间 等分若干份。1s=1000ms。假设按照200ms为一个区间。则子窗口的长度就为200ms。
则在时间跨度为1s的区间内，被分为5等份。



