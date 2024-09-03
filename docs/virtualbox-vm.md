# Create an Ubuntu VM in VirtualBox

[Download VirtualBox](https://www.virtualbox.org/wiki/Downloads) and install
it.

_I recommend using [UTM](https://mac.getutm.app/) instead on Apple Silicon._

Then download Ubuntu Server 24.04 LTS from
<https://ubuntu.com/download/server#manual-install>.

_Get the ARM version for Apple Silicon._

Start VirtualBox.
Click "New" button.
Select the `.iso` file you just downloaded in the "ISO Image" field.
And check "Skip Unattended Installation".
Then "Next" through the rest of the steps.

![Create VM from Ubuntu ISO](./vb-create-vm.png)

When you're done with the wizard a new window will pop up with the screen of
the VM.
At this point you need to open the Settings dialog and change the network
adapter to bridged.

![Bridged network adapter](./vb-bridged-network.png)

Using bridged network adapter allows you to connect to ports on the VM from
your host OS.

Click "Start" to start the VM.
Wait until it is booted.

1. Select "English" as language
2. Pick whatever keyboard layout you are accustomed to.
3. Choose "Ubuntu Server" as installation type.
4. Defaults for Network, Proxy, Mirror and Storage configuration.
5. For Profile configuration, type a username and password you can remember and give it a hostname.
6. Skip "Upgrade to Ubuntu Pro"
7. Check [x] to "Install OpenSSH server"

![Install OpenSSH server](./vb-ssh-config.png)

8. Don't select any "Featured server snaps"
9. Wait until it says "Installation complete!", then "Reboot Now".
10. After reboot, login with your credentials.
11. Take note of the IPv4 address shown, since you'll need it for later.

Congrats! You now got yourself a VM running Ubuntu Server.

Navigate back to the main guide and continue.
