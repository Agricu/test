# TrollStore 支持设备与 iOS 版本对应表

TrollStore并非越狱工具，而是借助CoreTrust漏洞实现永久签名安装应用的工具，其安装方式需根据设备芯片（arm64/arm64e）和iOS版本选择，详细对应关系如下：


| iOS 版本范围               | arm64 (A8)       | arm64 (A9-A11)   | arm64e (A12-A17/M1-M2) |
|----------------------------|------------------|------------------|------------------------|
| 14.0 beta 1 及更早         | 不支持           | 不支持           | 不支持                 |
| 14.0 beta 2 - 14.8.1       | TrollInstallerX  | TrollHelperOTA   | -                      |
| 15.0 - 15.5 beta 4         | TrollHelperOTA   | TrollHelperOTA   | TrollHelperOTA         |
| 15.5 - 15.5                | TrollInstallerMDC| TrollInstallerX  | TrollHelperOTA         |
| 15.6 beta 1 - 15.6 beta 3  | TrollHelperOTA   | TrollHelperOTA   | TrollHelperOTA         |
| 15.6 beta 4 - 15.6.1       | TrollInstallerMDC| TrollInstallerX  | TrollHelperOTA         |
| 15.7 - 15.7.1              | TrollInstallerMDC| TrollInstallerX  | -                      |
| 15.7.2 - 15.8.4            | TrollMisaka      | TrollInstallerX  | -                      |
| 16.0 beta 1 - 16.0 beta 3  | 不适用           | TrollInstallerX  | TrollHelperOTA         |
| 16.0 beta 4 - 16.6.1       | 不适用           | TrollInstallerX  | -                      |
| 16.7 RC - 16.7 RC          | 不适用           | TrollRestore     | -                      |
| 16.7 - 16.7.11             | 不适用           | 不支持           | -                      |
| 17.0 beta 1 - 17.0 beta 4  | 不适用           | TrollInstallerX  | TrollRestore           |
| 17.0 beta 5 - 17.0         | 不适用           | TrollRestore     | TrollRestore           |
| 17.0.1 及更高              | 不适用           | 不支持           | 不支持                 |


## 说明
1. 「不适用」：该芯片型号无对应iOS版本适配
2. 「-」：该芯片与iOS版本组合无需特定安装工具（或无对应工具）
3. 16.7.x（除16.7 RC (20H18)）及17.0.1以上版本，均不支持TrollStore
