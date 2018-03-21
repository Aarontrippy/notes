# raspi-setup

1. FRESH PI setup and installation
2. download the image: http://downloads.raspberrypi.org
3. Find the disk with 'diskutil list' on macOS
4. DD use dd to get the image https://www.raspberrypi.org/documentation/installation/installing-images/mac.md
sudo dd bs=1M if=/Users/john/Downloads/2018-03-13-raspbian-stretch-lite.img of=/dev/disk4 conv=sync
1. Install FUSE for mac or mount the boot volume on your laptop
2. enable ssh access: touch /boot/ssh in /boot: https://www.raspberrypi.org/documentation/remote-access/ssh/
3. Boot the pi on ethernet, and find it on the network with arp -a | grep b8:27:eb or similar
4. Clear out known_hosts on your laptop if needed to avoid warning for that IP address
5. Log in with username pi password raspberry
6. Run sudo raspi-config and change the hostname and locale, enlarge filesystem, then reboot
7. ssh back in with pi@hostnameofpi.local
8. Make an ssh key and set up ssh, then do ssh-copy-id to out it on the pi
9. Use raspi-config to update the system
10. Put ssh on it
11. Apt-get update
12. Install vim, tmux, git
13. Set up GitHub access: https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/
14. Edit /etc/wpa_supplicant/wpa_supplicant.conf: https://www.raspberrypi.org/documentation/configuration/wireless/wireless-cli.md or get mine from https://gist.github.com/johnelliott/152cd38e479e18aa1ef28e4799dba3e6 with r!wpa_supplicant said passphrase into vim
