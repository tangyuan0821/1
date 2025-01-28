### 一种绕过维基百科IP封禁的方式（LInux）

#### 安装 Clash

1. 下载 Clash for Linux：
   
   - 访问 [Clash GitHub 发布页面](https://github.com/Dreamacro/clash/releases)，下载适用于 Linux 的版本（如 `clash-linux-amd64`）。
   - 解压并赋予执行权限：
     ```bash
     tar -xvzf clash-linux-amd64.tar.gz
     chmod +x clash-linux-amd64
     ```
2. 配置 Clash：
   
   - 创建一个配置文件（如 `config.yaml`），内容可以参考 Clash 的官方文档或从 Clash for Windows 的配置中导出。
   - 启动 Clash：
     ```bash
     ./clash-linux-amd64 -d .
     ```
3. 设置系统代理：
   
   - 在 Linux 系统中，可以通过环境变量设置代理：
     ```bash
     export http_proxy=http://127.0.0.1:7890
     export https_proxy=http://127.0.0.1:7890
     ```

---

### 2. 使用 OpenVPN 或 SoftEther VPN

SoftEther VPN 也支持 Linux 系统，可以通过命令行或 GUI 工具连接 VPN Gate 服务器。

#### 安装 SoftEther VPN Client

1. 下载 SoftEther VPN Client for Linux：
   
   - 访问 [SoftEther VPN 下载页面](https://www.softether-download.com/)，选择 Linux 版本。
   - 解压并安装：
     ```bash
     tar -xvzf softether-vpnclient.tar.gz
     cd vpnclient
     make
     ```
2. 启动 SoftEther VPN Client：
   
   ```bash
   ./vpnclient start
   ```
3. 连接 VPN Gate 服务器：
   
   - 使用命令行工具 `vpncmd` 连接到 VPN Gate 服务器：
     ```bash
     ./vpncmd
     ```
   - 按照提示输入服务器地址和端口，选择 VPN Gate 服务器并连接。

---

### 3. 使用其他 VPN 工具

如果你不想使用 SoftEther VPN，可以选择其他支持 Linux 的 VPN 工具，例如：

- **OpenVPN**：支持从 VPN Gate 下载配置文件并连接。
- **WireGuard**：轻量级 VPN 工具，支持 Linux。

#### 使用 OpenVPN 连接 VPN Gate

1. 下载 VPN Gate 的 OpenVPN 配置文件：
   
   - 访问 [VPN Gate 网站](https://www.vpngate.net/)，下载适用于 Linux 的 OpenVPN 配置文件（`.ovpn` 文件）。
2. 安装 OpenVPN：
   
   ```bash
   sudo apt update
   sudo apt install openvpn
   ```
3. 连接 VPN：
   
   ```bash
   sudo openvpn --config your-config-file.ovpn
   ```

---

### 4. 注册维基百科账号

1. 通过上述方法连接到 VPN 或代理后，访问 [维基百科注册页面](https://zh.wikipedia.org/w/index.php?title=Special:%E5%88%9B%E5%BB%BA%E8%B4%A6%E6%88%B7)。
2. 完成注册后，在用户讨论页上挂{{封禁申诉|申请IPBE+封禁IP地址}}模板，申请 IP 封禁豁免。
