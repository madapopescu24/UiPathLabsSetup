Help
{: .eyebrow }

# 🛠️ Troubleshooting

**Look up your symptom here before you raise your hand. If it isn't listed, or the fix doesn't work, ask the trainer.**

## 🖥️ The VM

<div class="fix-grid" markdown>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Ctrl+V doesn't paste into the VM in Azure Bastion</span>

<span class="lbl">Cause</span> Chrome on your own machine blocks the Bastion site from your clipboard

<span class="lbl">Fix</span> Open `chrome://settings/content/clipboard` on your own machine, remove the Bastion site from **Not allowed to see your clipboard**, and reload the tab

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Signing in to the VM fails</span>

<span class="lbl">Cause</span> The username or password isn't the VM's, for example the workshop account's, or the password was typed by hand

<span class="lbl">Fix</span> Enter the **Username** from **Sandbox sign-in** (`admin_1`), paste the **Password** with its copy button, and try again

</div>

</div>

## 🔑 Signing in

<div class="fix-grid" markdown>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 You're signed in with your own account</span>

<span class="lbl">Cause</span> Chrome reused an account it already knew

<span class="lbl">Fix</span> Sign out, then sign in with **Continue with Microsoft** and the **Username** from **UiPath sign-in**

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 A workshop tenant is missing from the Tenant picker</span>

<span class="lbl">Cause</span> You're signed in with another account, or your workshop account wasn't added to that tenant

<span class="lbl">Fix</span> Check that you signed in with the **Username** from **UiPath sign-in**. If **{{ agentic_tenant }}** or **{{ training_tenant }}** is still missing, tell the trainer

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 You're on another tenant</span>

<span class="lbl">Cause</span> The account opened its last-used tenant

<span class="lbl">Fix</span> In the **Tenant** picker, in the upper-right corner, switch to the tenant the trainer names: **{{ agentic_tenant }}** or **{{ training_tenant }}**

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Studio Web goes blank or shows an old screen</span>

<span class="lbl">Cause</span> A known Studio Web display issue

<span class="lbl">Fix</span> Open Studio Web in a fresh tab, and check the **Tenant** picker shows the tenant for your workshop

</div>

</div>

!!! info "Still stuck?"
    Raise your hand. The trainer can check your VM, your workshop account, and your tenant access.
