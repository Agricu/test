<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>TrollStore 支持设备与 iOS 版本对应表</title>
    <style>
        /* 全局样式优化 */
        body {
            font-family: "Microsoft YaHei", Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            color: #333;
        }
        /* 标题样式 */
        .title {
            text-align: center;
            font-size: 24px;
            font-weight: bold;
            margin: 20px 0;
            color: #2c3e50;
        }
        /* 分隔线样式 */
        .divider {
            border: none;
            border-top: 2px solid #eee;
            margin: 25px 0;
        }
        /* 说明文字样式 */
        .intro {
            font-size: 16px;
            margin: 15px 0;
            text-align: left;
        }
        /* 表格样式 */
        .compatibility-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            font-size: 14px;
        }
        .compatibility-table th,
        .compatibility-table td {
            border: 1px solid #ddd;
            padding: 12px 15px;
            text-align: center; /* 表格内容居中 */
        }
        .compatibility-table th {
            background-color: #f8f9fa;
            font-weight: bold;
            color: #2c3e50;
        }
        .compatibility-table tr:nth-child(even) {
            background-color: #fafafa; /* 奇偶行交替背景色，提升可读性 */
        }
        /* 说明模块标题 */
        .note-title {
            font-size: 18px;
            font-weight: bold;
            margin: 25px 0 15px;
            color: #2c3e50;
        }
        /* 说明列表样式 */
        .note-list {
            list-style-type: decimal;
            padding-left: 25px;
            font-size: 15px;
            line-height: 1.8;
        }
    </style>
</head>
<body>
    <!-- 标题 -->
    <div class="title">TrollStore 支持设备与 iOS 版本对应表</div>

    <!-- 分隔线 -->
    <hr class="divider">

    <!-- 介绍文字 -->
    <div class="intro">
        TrollStore并非越狱工具，而是借助CoreTrust漏洞实现永久签名安装应用的工具。<br>
        其安装方式需根据设备芯片（arm64/arm64e）和iOS版本选择，详细对应关系如下：
    </div>

    <!-- 兼容性表格 -->
    <table class="compatibility-table">
        <thead>
            <tr>
                <th>iOS 版本范围</th>
                <th>arm64 (A8)</th>
                <th>arm64 (A9-A11)</th>
                <th>arm64e (A12-A17/M1-M2)</th>
            </tr>
        </thead>
        <tbody>
            <tr><td>14.0 beta 1 及更早</td><td>不支持</td><td>不支持</td><td>不支持</td></tr>
            <tr><td>14.0 beta 2 - 14.8.1</td><td>TrollInstallerX</td><td>TrollHelperOTA</td><td>-</td></tr>
            <tr><td>15.0 - 15.5 beta 4</td><td>TrollHelperOTA</td><td>TrollHelperOTA</td><td>TrollHelperOTA</td></tr>
            <tr><td>15.5 - 15.5</td><td>TrollInstallerMDC</td><td>TrollInstallerX</td><td>TrollHelperOTA</td></tr>
            <tr><td>15.6 beta 1 - 15.6 beta 3</td><td>TrollHelperOTA</td><td>TrollHelperOTA</td><td>TrollHelperOTA</td></tr>
            <tr><td>15.6 beta 4 - 15.6.1</td><td>TrollInstallerMDC</td><td>TrollInstallerX</td><td>TrollHelperOTA</td></tr>
            <tr><td>15.7 - 15.7.1</td><td>TrollInstallerMDC</td><td>TrollInstallerX</td><td>-</td></tr>
            <tr><td>15.7.2 - 15.8.4</td><td>TrollMisaka</td><td>TrollInstallerX</td><td>-</td></tr>
            <tr><td>16.0 beta 1 - 16.0 beta 3</td><td>不适用</td><td>TrollInstallerX</td><td>TrollHelperOTA</td></tr>
            <tr><td>16.0 beta 4 - 16.6.1</td><td>不适用</td><td>TrollInstallerX</td><td>-</td></tr>
            <tr><td>16.7 RC - 16.7 RC</td><td>不适用</td><td>TrollRestore</td><td>-</td></tr>
            <tr><td>16.7 - 16.7.11</td><td>不适用</td><td>不支持</td><td>-</td></tr>
            <tr><td>17.0 beta 1 - 17.0 beta 4</td><td>不适用</td><td>TrollInstallerX</td><td>TrollRestore</td></tr>
            <tr><td>17.0 beta 5 - 17.0</td><td>不适用</td><td>TrollRestore</td><td>TrollRestore</td></tr>
            <tr><td>17.0.1 及更高</td><td>不适用</td><td>不支持</td><td>不支持</td></tr>
        </tbody>
    </table>

    <!-- 分隔线 -->
    <hr class="divider">

    <!-- 说明模块 -->
    <div class="note-title">说明</div>
    <ul class="note-list">
        <li>「不适用」：该芯片型号无对应iOS版本适配</li>
        <li>「-」：该芯片与iOS版本组合无需特定安装工具（或无对应工具）</li>
        <li>16.7.x（除16.7 RC (20H18)）及17.0.1以上版本，均不支持TrollStore</li>
    </ul>
</body>
</html>
