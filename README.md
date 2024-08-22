# linux multimedia keys fix
a script to make linux not that much confused about 60% keyboard's Fn keys

simply copy paste this into your terminal:

```echo 0 | sudo tee /sys/module/hid_apple/parameters/fnmode && echo "options hid_apple fnmode=0" | sudo tee -a /etc/modprobe.d/hid_apple.conf && sudo update-initramfs -u```

if you're on arch, the update-initramfs gets replaced with ``` mkinitcpio -P```

script obtained from https://mikeshade.com/posts/keychron-linux-function-keys/
