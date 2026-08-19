# 🚀 VLESS 节点与优选域名工具 (ip-to-wl)

高效、便捷的 VLESS 节点批量处理与优选域名提取工具。

---

## ✨ 核心功能

* **批量生成新节点**：基于 1 个完整 VLESS 节点与多个 `域名(IP):端口#名称`，自动替换域名/IP、端口及节点名称，同时**完全保留**原节点的所有配置参数（UUID、Path、TLS、Header 等）。
* **批量提取优选信息**：输入多个 VLESS 节点，自动解析并提取其中的 `域名(IP):端口#名称` 信息，格式化输出。
* **灵活的多行批量处理**：支持换行分割多行数据，可无缝处理任意数量的节点与优选域名。

---

## 🛠️ 功能说明与示例

### 1. 生成新节点

**输入：**
* **基础 VLESS 节点** (1条)：
  ```text
  vless://uuid@example.com:443?encryption=none&security=tls&type=ws&host=example.com&path=%2F#原始节点
* **优选域名列表** (多条)：
  ```text
  1.1.1.1:8443#香港01
  cf.example.org:2053#美西02

### 2. 提取优选信息
* **基础 VLESS 节点** (多条)：
**输入：**
  ```text
  vless://uuid@1.1.1.1:8443?encryption=none&security=tls&type=ws#香港01  
  vless://uuid@cf.example.org:2053?encryption=none&security=tls&type=ws#美西02
**输出：**
  ```text
  1.1.1.1:8443#香港01
  cf.example.org:2053#美西02

** 📖 使用指南 **
1、输入数据时，请确保每行仅包含一个节点或一个 域名(IP):端口#名称 格式的记录。

2、批量处理时，直接使用换行符分割多行数据即可
