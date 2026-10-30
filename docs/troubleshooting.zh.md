帮助
{: .eyebrow }

# 🛠️ 故障排除 { #troubleshooting }

**举手之前，先在这里查找你遇到的症状。如果没有列出，或者解决方法无效，请问讲师。**

## 🖥️ 虚拟机 { #the-vm }

<div class="fix-grid" markdown>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Ctrl+V 无法粘贴到虚拟机</span>

<span class="lbl">原因</span> 你自己电脑上的 Chrome 阻止了 Bastion 网站访问你的剪贴板

<span class="lbl">解决</span> 在你自己的电脑上打开 `chrome://settings/content/clipboard`，把 Bastion 网站从 **Not allowed to see your clipboard** 中移除，然后重新加载标签页

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Bastion 登录失败</span>

<span class="lbl">原因</span> 用户名或密码不是虚拟机的，例如用了工作坊账号的

<span class="lbl">解决</span> 用复制按钮从虚拟机信息中复制 **Username** 和 **Password**，然后重试

</div>

</div>

## 🔑 登录 { #signing-in }

<div class="fix-grid" markdown>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 你用自己的账号登录了</span>

<span class="lbl">原因</span> Chrome 重用了它已经记住的账号

<span class="lbl">解决</span> 退出登录，然后通过 **Continue with Microsoft** 用 **Your Workshop Account** 中的用户名登录

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Studio Web 显示的是其他租户</span>

<span class="lbl">原因</span> 账号打开了上次使用的租户

<span class="lbl">解决</span> 在右上角的租户选择器中切换到 **{{ training_tenant }}**

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Studio Web 出现空白或显示旧页面</span>

<span class="lbl">原因</span> Studio Web 的一个已知显示问题

<span class="lbl">解决</span> 在新标签页中打开 Studio Web，并检查租户选择器显示的是 **{{ training_tenant }}**

</div>

</div>

## 💻 Codex 和 uip CLI { #codex-and-the-uip-cli }

<div class="fix-grid" markdown>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 `uip login status` 显示的组织或租户不对</span>

<span class="lbl">原因</span> CLI 登录到了别的地方

<span class="lbl">解决</span> 再次运行[编码智能体与 CLI](coding-agent-and-cli.md#sign-the-uip-cli-in) 中的 `uip login` 命令。如果仍然显示错误的租户，告诉讲师。不要在错误的租户上构建任何内容。

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 在 Codex 中，`uip` 命令因 DNS 或 *"fetch failed"* 错误而失败</span>

<span class="lbl">原因</span> Codex 沙盒没有网络访问权限

<span class="lbl">解决</span> 退出 Codex，并以启用网络访问的方式重新启动：`codex -c sandbox_workspace_write.network_access=true`

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Codex 不知道 UiPath skills</span>

<span class="lbl">原因</span> Codex 运行所在的文件夹中没有安装这些 skills

<span class="lbl">解决</span> 让 Codex 运行 `uip skills install --agent codex --path . --repo https://github.com/UiPath/skills.git`，然后在同一个文件夹中重新启动 Codex

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 `/status` 显示的是其他模型</span>

<span class="lbl">原因</span> Codex 以默认模型启动了

<span class="lbl">解决</span> 输入 `/model`，选择讲师指定的模型和推理强度，然后用 `/status` 检查。不要在未告知讲师的情况下使用其他模型继续操作。

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Codex 说它在等待某件事，一等就是几分钟</span>

<span class="lbl">原因</span> 它在轮询一个不会改变的状态

<span class="lbl">解决</span> 让它停止等待，并报告已有的结果。必要时按 **Esc** 中断它。

</div>

</div>

!!! info "还是没解决？"
    请举手。讲师可以检查你的虚拟机、工作坊账号和租户访问权限。
