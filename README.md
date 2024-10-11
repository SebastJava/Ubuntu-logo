> Ubuntu means "a humanist and ethic philosophy concentrating on the relations and allegiances of the people with each other". The Ubuntu logo can be described as the graphical illustration of three people holding their arms out and making a circle.

![Presentation-Ubuntu-logo-v2022-vs-v2024](Presentation/Presentation-Ubuntu-logo-v2022-vs-v2024.png)

## The Ubuntu logo redone in a more precise way

There is no innovation here. It is still the same logo, with just a few pixels difference.

The 2022 version of the logo is excellent, it is a good concept that does not need to be explained. But its execution is not perfect. A keen eye sees subtle approximations, and that is disturbing.

![Presentation-Ubuntu-logo-v2022-wrong](Presentation/Presentation-Ubuntu-logo-v2022-wrong.png)

The current version of the Ubuntu logo, this 2022 version, has undergone a subtle, almost invisible rotation, and it looks like a mistake or an imperfection, IMHO. In comparison, the previous version from 2010 was made of perfect values everywhere. The 3 circles, or heads, had perfectly symmetrical rotation angles of 30°, 150°, and 270° degrees. But that's not the case here with this current version from 2022. The rotation angles are weird. It feels like a mistake. Those angles are roughly set at something like 32.75°, 152.75°, 272.75°...

![Presentation-Ubuntu-logo-v2024-twisted](Presentation/Presentation-Ubuntu-logo-v2024-twisted.png)

If you wanted the logo to look less formal, less symmetrical, then I would suggest adding an obvious rotation, say 15 degrees. Otherwise, it just looks like a mistake to me.

Don't get me wrong, I think your logo is pretty good as is. It isn't ugly at all and it clearly carries some significance, some positive values. I don't want to change anything to this concept. I don't even want this assymetrical alternative showed here. I just want to push this standard 2024 version as showed here on top of this page: [logo-v2024.svg](logo-v2024.svg). That's the same logo as the current one, but redone in a perfectly precise way.

> **Precise**
> Ubuntu is crisp and clean in engineering and attitude. There is beauty in the precision of the process and product.

> Our values should be evident wherever Ubuntu is encountered, whether online or via traditional marketing material.

> The Ubuntu logo is striking and clear, and it represents the brand’s core
> values.

source: https://design.ubuntu.com/brand

### Method

I tried to do things simply, using the appropriate tools, in order to simplify my operations and thus reduce the possibilities of errors.

* **Everything was created in Inkscape,** on a semi-opaque layer above the original 2022 logo, in order to ensure very similar measurements.

* The 3 small circles are identical duplicates. Their center of rotation is snapped to the center of rotation of the large circle. They rotate at exactly 120° from each other.

* The large circle was converted to a path (Path > Stroke to path), then cut out using Path > Difference.

* The 8 logos to be changed were downloaded from https://design.ubuntu.com/resources. Only the logos were replaced, the typography remains unchanged.

That's just a quick summary, of course.

### URL resources

version 2024: [design.ubuntu.com-v2024](design.ubuntu.com-v2024) (proposed new version)  
version 2022: https://design.ubuntu.com/resources (current version)  
version 2010: https://en.m.wikipedia.org/wiki/File:UbuntuCoF.svg (old version)  

### Update your local files

**First**, [Download](https://github.com/SebastJava/Ubuntu-logo/archive/refs/heads/main.zip) this repository as a ZIP file and extract it.

**Next**, open your terminal into this directory. Example:

```
cd ~/Downloads/Ubuntu-logo-main
```

**Replace the "Show Apps" icon:**

```
sudo cp start-here-symbolic.svg /usr/share/icons/Yaru/scalable/places/start-here-symbolic.svg
```

NOTE: If you are using [Dash-to-Panel](https://extensions.gnome.org/extension/1160/dash-to-panel/) you can easily choose your start icon from there. You can use the standard `start-here-symbolic.svg` or one of the variants in the `start-here-variants` directory.

**Boot sequence and login screen:**

```
sudo cp ubuntu-logo-v2024-plymouth.png /usr/share/plymouth/themes/spinner/watermark.png
sudo cp ubuntu-logo-v2024-plymouth.png /usr/share/plymouth/ubuntu-logo.png
```

You must update your initramfs after having changed this Plymouth theme:

```
sudo update-initramfs -u
```

WARNING: Please disable your Kernel Livepatch to avoid some weird Plymouth on first restart... (Go to Software & Updates > Ubuntu Pro)

RESTART your computer to see your updated logos on the boot sequence, login screen and dash.

![Dash-example-2](Dash-example-3.png)
