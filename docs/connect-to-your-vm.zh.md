第 2 步，共 3 步
{: .eyebrow }

# 🖥️ 连接到虚拟机 { #connect-to-your-vm }

**用远程桌面打开你的虚拟机，或者通过 Azure Bastion 在浏览器标签页中打开。从这里开始，你都在虚拟机里操作。**

## 🔌 选择连接方式 { #choose-how-to-connect }

打开你的工作坊页面。**Sandbox sign-in** 中显示虚拟机的 **Username** 和 **Password**，并带有复制按钮。

![Sandbox 一行中的 Connect in browser 和 Remote Desktop file，以及 Sandbox sign-in 中的 Connection address、Username admin_1 和隐藏的 Password，带复制按钮](images/workshop-sandbox-details.png){ .screenshot width="480" }

推荐使用远程桌面。如果你无法使用远程桌面客户端，再使用 Azure Bastion。

=== "🖥️ Remote Desktop（推荐）"

    1. 在 **Sandbox** 旁边，选择 **Remote Desktop file**。
    2. 打开下载的 `.rdp` 文件。在 Windows 上，它会在 **Remote Desktop Connection** 中打开；在 Mac 上，会在 **Windows App** 中打开。
    3. 要求输入凭据时，输入 **Sandbox sign-in** 中的 **Username**：`admin_1`。
    4. 选择 **Sandbox sign-in** 中 **Password** 旁边的复制按钮，粘贴密码，然后选择 **Continue**。

        ![Enter Your Credentials 对话框，Username 为 admin_1，Password 字段为空，以及 Continue 按钮](images/rdp-credentials.png){ .screenshot width="440" }

    5. 如果提示无法验证虚拟机的证书，选择 **Continue**。
    6. 等待虚拟机的 Windows 桌面加载完成。

=== "🌐 Azure Bastion"

    Azure Bastion 会在 Chrome 标签页中打开虚拟机，所以你不需要远程桌面客户端。

    1. 在 **Sandbox** 旁边，选择 **Connect in browser**。
    2. 在 **Azure Bastion** 表单中，保持 **Protocol** 为 **RDP**、**Port** 为 **3389**。输入 **Sandbox sign-in** 中的 **Username** 和 **Password**，选择你的 **Keyboard Language**，然后选择 **Login**。

        ![Azure Bastion 登录表单，包含 Protocol RDP、Port 3389、Username、Password、Keyboard Language 和 Login 按钮](images/azure-bastion-login.png){ .screenshot width="420" }

    3. 浏览器询问是否允许访问剪贴板时，选择允许。
    4. 等待虚拟机的 Windows 桌面在浏览器标签页中加载完成。

    !!! warning "无法用 Ctrl+V 粘贴到虚拟机？"
        在你自己电脑上的 Chrome 中打开 `chrome://settings/content/clipboard`，确认 Bastion 网站不在 **Not allowed to see your clipboard** 列表中。然后重新加载 Bastion 标签页。

## 🧰 虚拟机桌面 { #your-vm-desktop }

虚拟机打开后，你会看到它的 Windows 桌面。动手练习工作坊都在这里进行。在 **Sandbox created** 邮件中写明的日期之前，你的工作会一直保留在虚拟机上。

![虚拟机的 Windows 桌面，包含 Google Chrome、UiPath Studio、UiPath Assistant、Visual Studio Code、Git Bash、Excel 等工具的快捷方式](images/vm-desktop.png){ .screenshot width="640" }

你需要的工具都已经装好，桌面上有它们的快捷方式：**Google Chrome**、**UiPath Studio**、**UiPath Assistant**、**Visual Studio Code**、**Git Bash** 和 **Excel**。你不需要安装任何东西。

## 📋 检查复制和粘贴 { #check-copy-and-paste }

在你自己的电脑上复制一些内容，然后粘贴到虚拟机中，例如粘贴到 Windows 搜索框里。如果能粘贴进去，这一步就完成了。

!!! success "可以进入下一步了"
    虚拟机的桌面已经打开，并且可以粘贴内容。从现在起，每一步都在虚拟机中完成。下一步：[登录](sign-in.md)。
