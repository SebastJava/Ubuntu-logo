The latest version of the Ubuntu logo, this 2022 version, has undergone a subtle, almost invisible rotation, and it looks like a mistake or an imperfection, IMHO.

Don't get me wrong, I have nothing against the orange rectangle that replaces the big orange circle, in the background. And I have nothing against a "Circle of Friends" (CoF) that is off-center in relation to this rectangle. No, what bothers me is the angle of rotation of these three heads. I would expect a 0°, 120°, 240°... or rather a 30°, 150°, 270°... That was exactly what you had on the previous version, the 2010 version, but the new 2022 version hides a small error, with angles that I estimate to be something like 32.75°, 152.75°, 272.75°... But please see the attached images, as it is better explained with images.

### URLs

version 2022: https://design.ubuntu.com/resources
version 2022: https://assets.ubuntu.com/v1/a7e3c509-Canonical%20Ubuntu.svg
(version 2022 = current version)

version 2010: https://en.m.wikipedia.org/wiki/File:UbuntuCoF.svg
version 2010: https://upload.wikimedia.org/wikipedia/commons/9/9e/UbuntuCoF.svg

versions 2004-vs-2010-vs-2022: https://www.reddit.com/r/linux/comments/tfkwgk/ubuntu_has_a_brand_new_logo/

### Local files

**Plymouth theme, i.e. boot sequence:**
/usr/share/plymouth/themes/spinner/watermark.png
```
# You must update your Plymouth theme after having changed this watermark.png... 
sudo update-initramfs -u
# WARNING: You will get some error message on the first restart, but it looks okay after that !?
```
**login screen:**
/usr/share/plymouth/ubuntu-logo.png

**Show Apps icon:**
/usr/share/icons/* (many places) start-here.svg, start-here-dark.svg, start-here-symbolic.svg

(I can't remember exactly which `start-here.svg` should be changed because I am using https://extensions.gnome.org/extension/1160/dash-to-panel/ and I get to choose my icon from there...)
