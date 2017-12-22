* Peer 初始化
```java
public synchronized void reset() {
    // 本地阻塞
    this.choking = true;
    // 本地没兴趣
    this.interesting = false;
    // 远程阻塞
    this.choked = true;
    // 远程没兴趣
    this.interested = false;

    this.exchange = null;

    this.requests = null;
    this.lastRequestedOffset = 0;
    this.downloading = false;
}
```