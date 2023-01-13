# Pwnbox

## Heavy modified to work with my "fresh install new setup" scripts.

## Setup OpenVPN

We also need to add your vpn file to your /etc/openvpn location:

`sudo cp [your VPN FILE].ovpn /etc/openvpn/`

`sudo mv /etc/openvpn/[your VPN file].ovpn /etc/openvpn/[your VPN file].conf`

Make sure you rename your file to `.conf`. Then you can start your VPN like you would normally do.

You should now see a theme called "HackTheBox". Select it and select "Apply Background".

## Customizing panels

On the top panel, right click one of the three system monitors graphs (the ones showing your 'process', 'memory', and 'network'). Select "Remove from Panel".

Next, on the top panel, right click the "shell" icon (the one that looks like a bash prompt). Select "Properties".

> NOTE : You will see the "Launcher Properties" pop up. This is where you can really customize your ParrotOS. You don't need to follow what Hack the Box did. You can add ANY script you want, any command, icon, etc, to your OS! This is how you can truly personalize it.

Click on the bash icon to the left, and a window should pop up asking you to select an icon. Navigate to /usr/share/icons/htb/ and choose `bash.svg`.

- ## To get the 'ping panel'

    Right click on a blank space on the top panel and choose "Add to Panel". In the search bar, type "command", select "command" then click "add". The current time should populate on the top panel. Right click on it, and in the command section, paste in `/opt/vpnpanel.sh`, with an interval of "5" seconds. It should show "HTB VPN: Disconnected" unless you are on the vpn.

- ## To get the "processor" menu

    Right click on a blank space on the top panel and search for "System monitor". Select it and add it. Right click on the little black box that appeared, select "preferences" and under "System monitor width", update it to "135" pixels, and updated the field below it to "100" milliseconds.

- ## 'Plank', the MacOS bar on the bottom

    Start by deleting the bottom panel by `right clicking` and selecting `delete this panel`.

    `sudo apt install plank -y`

    Once Plank is installed, on the top bar, go to "System -> Preferences -> Personal -> Startup Application". Right hand side, select "Add" and fill in the values:

    - Name: Plank
    - Command: plank
    - Delay: 0

    Plank will now startup whenever you reboot your machine.
