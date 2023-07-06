##                                核心测试文档V0.0.1

### 测试助记词

* invest later bring calm twin magnet matter mechanic nuclear burden title carbon
* 建议用自己的助记词，以上助记词测试人员较多，操作过于频繁，会互相影响。

### 测试工具

- Android：
  - Termux
  - PingTools
  - Net Analyzer
- iOS:
  - Net Analyzer 
  - Network Tools 
- Mac：
  - 终端
- Windows：
  - 终端

### 测试内容模版

1. 测试组网
   - 使用Ping命令测试组网连通性：
     ```
     ping 100.64.0.2
     ```

2. 测试这台机器部署的web服务
   - 访问该机器的Web服务地址：
     ```
     http://100.64.0.2:8080
     ```

3. 测试配置的Magic DNS是否生效
   - 访问配置的Magic DNS地址：
     ```
     http://2314.testnsio.gid:8080
     ```

4. 测试出口
   - 浏览器访问ipip.net查看自己设备的外网IP地址；
   - 然后选择设备IP为100.64.0.2的设备作为出口，再次浏览器访问ipip.net查看外网IP地址是否发生变化，验证自己设备的外网IP是否为35.247.149.216

5. 作为出口
   - 同上，只是自己设备作为出口，让别的设备选择。

6. 设置子网路由
   - 在100.64.0.2这台设备上，添加子网路由173.28.1.0/24
   - 然后访问访问这个子网里的服务如 http://173.28.1.2:8000或http://173.28.1.5:8000