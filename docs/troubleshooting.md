Help
{: .eyebrow }

# 🛠️ Troubleshooting

**Look up your symptom here before you raise your hand. If it isn't listed, or the fix doesn't work, ask the trainer.**

## 🖥️ The VM

<div class="fix-grid" markdown>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Ctrl+V doesn't paste into the VM</span>

<span class="lbl">Cause</span> Chrome on your own machine blocks the Bastion site from your clipboard

<span class="lbl">Fix</span> Open `chrome://settings/content/clipboard` on your own machine, remove the Bastion site from **Not allowed to see your clipboard**, and reload the tab

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 The Bastion login fails</span>

<span class="lbl">Cause</span> The username or password isn't the VM's, for example the workshop account's

<span class="lbl">Fix</span> Copy the **Username** and **Password** from your VM details with the copy buttons, and try again

</div>

</div>

## 🔑 Signing in

<div class="fix-grid" markdown>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 You're signed in with your own account</span>

<span class="lbl">Cause</span> Chrome reused an account it already knew

<span class="lbl">Fix</span> Sign out, then sign in with **Continue with Microsoft** and the username from **Your Workshop Account**

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Studio Web shows another tenant</span>

<span class="lbl">Cause</span> The account opened its last-used tenant

<span class="lbl">Fix</span> Switch to **{{ training_tenant }}** in the tenant picker, in the upper-right corner

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Studio Web goes blank or shows an old screen</span>

<span class="lbl">Cause</span> A known Studio Web display issue

<span class="lbl">Fix</span> Open Studio Web in a fresh tab, and check the tenant picker shows **{{ training_tenant }}**

</div>

</div>

## 💻 Codex and the uip CLI

<div class="fix-grid" markdown>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 `uip login status` shows the wrong organization or tenant</span>

<span class="lbl">Cause</span> The CLI is signed in somewhere else

<span class="lbl">Fix</span> Run the `uip login` command from [Coding agent and CLI](coding-agent-and-cli.md#sign-the-uip-cli-in) again. If it still shows the wrong tenant, tell the trainer. Don't build anything on the wrong tenant.

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 `uip` commands fail with DNS or *"fetch failed"* errors inside Codex</span>

<span class="lbl">Cause</span> The Codex sandbox has no network access

<span class="lbl">Fix</span> Exit Codex and start it again with network access: `codex -c sandbox_workspace_write.network_access=true`

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Codex doesn't know the UiPath skills</span>

<span class="lbl">Cause</span> The skills aren't installed in the folder Codex runs in

<span class="lbl">Fix</span> Ask Codex to run `uip skills install --agent codex --path . --repo https://github.com/UiPath/skills.git`, then restart Codex from the same folder

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 `/status` shows another model</span>

<span class="lbl">Cause</span> Codex started with its default model

<span class="lbl">Fix</span> Type `/model`, pick the model and reasoning effort the trainer names, and check with `/status`. Don't carry on with another model without telling the trainer.

</div>

<div class="fix" markdown>
<span class="f-title" markdown="span">🚨 Codex says it's waiting for something for minutes</span>

<span class="lbl">Cause</span> It's polling a state that won't change

<span class="lbl">Fix</span> Tell it to stop waiting and report what it has. Press **Esc** to interrupt it if needed.

</div>

</div>

!!! info "Still stuck?"
    Raise your hand. The trainer can check your VM, your workshop account, and your tenant access.
