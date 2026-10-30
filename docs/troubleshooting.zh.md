帮助
{: .eyebrow }

# 🛠️ 故障排除 { #troubleshooting }

**举手之前，先在这里查找你遇到的症状。如果没有列出，或者解决方法无效，请问讲师。**

## 🖥️ 虚拟机 { #the-vm }

<div class="fix-grid" markdown>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 在 Azure Bastion 中，Ctrl+V 无法粘贴到虚拟机</span>

<span class="lbl">原因</span> 你自己电脑上的 Chrome 阻止了 Bastion 网站访问你的剪贴板

<span class="lbl">解决</span> 在你自己的电脑上打开 `chrome://settings/content/clipboard`，把 Bastion 网站从 **Not allowed to see your clipboard** 中移除，然后重新加载标签页

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 登录虚拟机失败</span>

<span class="lbl">原因</span> 用户名或密码不是虚拟机的，例如用了工作坊账号的，或者密码是手动输入的

<span class="lbl">解决</span> 输入 **Sandbox sign-in** 中的 **Username**（`admin_1`），用复制按钮粘贴 **Password**，然后重试

</div>

</div>

## 🔑 登录 { #signing-in }

<div class="fix-grid" markdown>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 你用自己的账号登录了</span>

<span class="lbl">原因</span> Chrome 重用了它已经记住的账号

<span class="lbl">解决</span> 退出登录，然后通过 **Continue with Microsoft** 用 **UiPath sign-in** 中的 **Username** 登录

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Tenant 选择器中缺少某个工作坊租户</span>

<span class="lbl">原因</span> 你登录的是另一个账号，或者你的工作坊账号还没有被添加到该租户

<span class="lbl">解决</span> 检查你是否用 **UiPath sign-in** 中的 **Username** 登录。如果仍然缺少 **{{ agentic_tenant }}** 或 **{{ training_tenant }}**，告诉讲师

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 你在另一个租户上</span>

<span class="lbl">原因</span> 账号打开了上次使用的租户

<span class="lbl">解决</span> 在右上角的 **Tenant** 选择器中，切换到讲师指定的租户：**{{ agentic_tenant }}** 或 **{{ training_tenant }}**

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Studio Web 出现空白或显示旧页面</span>

<span class="lbl">原因</span> Studio Web 的一个已知显示问题

<span class="lbl">解决</span> 在新标签页中打开 Studio Web，并检查 **Tenant** 选择器显示的是你的工作坊所用的租户

</div>

</div>

!!! info "还是没解决？"
    请举手。讲师可以检查你的虚拟机、工作坊账号和租户访问权限。
