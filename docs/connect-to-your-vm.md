Step 2 of 4
{: .eyebrow }

# 🖥️ Connect to Your VM

**Open your VM in a browser tab with Azure Bastion. From here on, you work inside the VM.**

## 🔌 Connect through Azure Bastion

Azure Bastion opens the VM in a Chrome tab, so you don't need a Remote Desktop client.

1. Open your VM details. They show the VM's **Username** and **Password**, with copy buttons.
2. Select **Connect via Azure Bastion**.

    ![The VM details: a Username and a masked Password with copy buttons, and the Download RDP File and Connect via Azure Bastion buttons](images/vm-connect-options.png){ .screenshot width="320" }

3. In the **Azure Bastion** form, keep **Protocol** on **RDP** and **Port** on **3389**. Enter the VM's username and password, pick your **Keyboard Language**, and select **Login**.

    ![The Azure Bastion login form with Protocol RDP, Port 3389, Username, Password, Keyboard Language, and the Login button](images/azure-bastion-login.png){ .screenshot width="420" }

4. When your browser asks whether to allow clipboard access, accept it.
5. Wait for the VM's Windows desktop to load in the browser tab.

!!! tip "Prefer a Remote Desktop client?"
    **Download RDP File** gives you a file that opens the VM in Remote Desktop instead. Use it only if the trainer asks you to: Azure Bastion is the recommended way.

## 📋 Check copy and paste

Copy something on your own machine, then paste it into the VM, for example into the Windows search box. If it pastes, you're done.

!!! warning "Can't paste into the VM with Ctrl+V?"
    In Chrome on your own machine, open `chrome://settings/content/clipboard` and make sure the Bastion site isn't under **Not allowed to see your clipboard**. Then reload the Bastion tab.

!!! success "Ready for the next step"
    The VM's desktop is open in a Chrome tab, and pasting into it works. From now on, do every step inside the VM. Next: [sign in](sign-in.md).
