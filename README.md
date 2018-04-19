
[![Build Status](https://travis-ci.org/whitepages/flume-udp-source.png?branch=master)](https://travis-ci.org/whitepages/flume-udp-source)

Flume plugin allowing direct consumption of UDP messages.
Note that this software is under active development and should not be
considered ready for production use.

Developed for use with Apache Flume 1.4.

To use, add the following to flume.conf:

```
a1.sources = udp
a1.sources.udp.type = com.whitepages.flume.plugins.source.udp.UDPSource
a1.sources.udp.bind = localhost
a1.sources.udp.port = 5515
a1.sources.udp.maxsize = 65536
```

Adapted directly from original work by @ottomata
Many thanks for his work.
https://github.com/ottomata/flume-ng/tree/udp-source

This plugin is distributed under the same license as Apache Flume 1.4.

### 编译

执行`mvn package`编译，成功后得到如下三个关键文件：

```
target/flume-udp-source-1.0.0-SNAPSHOT.jar
target/flume-udp-source-1.0.0-SNAPSHOT-sources.jar
target/flume-udp-source-1.0.0-SNAPSHOT-javadoc.jar
```

将`flume-udp-source-1.0.0-SNAPSHOT.jar`添加到flume的lib目录下即可。

目前在flume的1.5.2和1.6.0版本上测试没有问题。
