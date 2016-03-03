## 3.7 PUBCOMP – 发布完成（QoS 2，第三步）

PUBCOMP报文是对PUBREL报文的响应。它是QoS 2等级协议交换的第四个也是最后一个报文。

### 3.7.1 固定报头

##### 图例 3.18 – PUBCOMP报文固定报头

| **Bit** | **7**                | **6**  | **5** | **4** | **3** | **2** | **1** | **0** |
|---------|----------------------|--------|-------|-------|-------|-------|-------|-------|
| byte 1  | MQTT控制报文类型 (7) | 保留位 |
|         | 0                    | 1      | 1     | 1     | 0     | 0     | 0     | 0     |
| byte 2  | 剩余长度 (2)         |
|         | 0                    | 0      | 0     | 0     | 0     | 0     | 1     | 0     |

**剩余长度字段**

表示可变报头的长度。对PUBCOMP报文这个值等于2。

### 3.7.2 可变报头

可变报头包含与等待确认的PUBREL报文相同的报文标识符。

##### 图例 3.19 – PUBCOMP报文可变报头

| **Bit** | **7**          | **6** | **5** | **4** | **3** | **2** | **1** | **0** |
|---------|----------------|-------|-------|-------|-------|-------|-------|-------|
| byte 1  | 报文标识符 MSB |
| byte 2  | 报文标识符 LSB |

### 3.7.3 有效载荷

PUBCOMP报文没有有效载荷。

### 3.7.4 动作

完整的描述见4.3.3节。


### 第三章目录 MQTT控制报文

- [3.0 Contents – MQTT控制报文](03-ControlPackets.md)
- [3.1 CONNECT – 连接服务端](0301-CONNECT.md)
- [3.2 CONNACK – 确认连接请求](0302-CONNACK.md)
- [3.3 PUBLISH – 发布消息](0303-PUBLISH.md)
- [3.4 PUBACK –发布确认](0304-PUBACK.md)
- [3.5 PUBREC – 发布收到（QoS 2，第一步）](0305-PUBREC.md)
- [3.6 PUBREL – 发布释放（QoS 2，第二步）](0306-PUBREL.md)
- [3.7 PUBCOMP – 发布完成（QoS 2，第三步）](0307-PUBCOMP.md)
- [3.8 SUBSCRIBE - 订阅主题](0308-SUBSCRIBE.md)
- [3.9 SUBACK – 订阅确认](0309-SUBACK.md)
- [3.10 UNSUBSCRIBE –取消订阅](0310-UNSUBSCRIBE.md)
- [3.11 UNSUBACK – 取消订阅确认](0311-UNSUBACK.md)
- [3.12 PINGREQ – 心跳请求](0312-PINGREQ.md)
- [3.13 PINGRESP – 心跳响应](0313-PINGRESP.md)
- [3.14 DISCONNECT –断开连接](0314-DISCONNECT.md)

### 项目主页

- [MQTT协议中文版](https://github.com/mcxiaoke/mqtt)

