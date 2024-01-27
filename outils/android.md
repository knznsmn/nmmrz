# Setting Up An Environment on Android

I am using a handy and fast Huawei Y9 2019 Prime. I can't root it because of Huawei's weird policy for unlocking their smartphones' bootloaders but fortunately, but I don't really need any special privilege to set up development environment for coding practices, and that's thanks to Termux. 

## Setting Up
### Package Manager
F-Droid is the one-stop package manager for Android. Download [F-Droid](https://f-droid.org/packages/org.fdroid.fdroid/).

Through F-Droid, download the terminal emulator `Termux`. 

[Termux](termux.md) _Download from F-Droid repo. **F-Droid repository.**_ Download it. Download it now.

Most virtual keyboards that come with Android (these also include Microsoft Swiftkey) are fine as Termux supplies the useful keys like `<Esc>`, `<Tab>`, and arrow keys independently anyway. Though I use some applications that require `<Esc>` like [Obsidian](outils/obsidian.md) so I soared the oceans and swam the skies to find an Android keyboard that sports the needed `<Esc>` keys. And alas at last, there exists a God-smile keyboard that is so glorious I can't be sure if it's okay not to mention it here. Install it. You need to install it.

[Unexpected Keyboard](https://f-droid.org/packages/juloo.keyboard2/). Install it. You need to install it now. It provides keys everyone should expect from anything that deems to be called a 'keyboard':
- `<Esc>` key
- `<Ctrl>` key
- easy and quick access to punctuations and enclosing symbols
- and so much more convenience only experienced by royalties in fantasy books.

Really. All the keys I expect on a keyboard. It's ironic the app is called 'Unexpected'. There must be some funny thoughts somewhere in there.

[Syncthing](https://f-droid.org/packages/com.nutomic.syncthingandroid/). Install it. Install it now. It's more versatile than any syncing applications I tried (which are just a few: iCloud, Google Drive, Microsoft OneDrive). I use it (I mean the Syncthing now, not those proprietary services) to sync files across devices (a [Linux machine](outils/linux.md), an Huawei smartphone, [iPhone 6s, and iPad 11](outils/ios.md)).

### Setting Up Termux

Termux is proof that there is paradise on Earth. Look at iOS and/or iPadOS, so beautiful but barren.

Even without `root`, Termux is so much fun and powerful to use. I can install all the tools I need:

```bash
apt install git openssh gcc vim neofetch
```

Setting up `git`, `vim`, and `ssh` are the same steps as in my Linux machine.

So is `oh-my-bash` for pretty terminal look:

```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"
```

#### Configuring motd
Modifying `motd` (message of the day) in Termux is straightforward but I'll still write it here 'cause that's what this notebook is for: no memorization. Just create a `motd.sh` file inside the `.termux` directory.

```bash
cd ~/.termux
```

```bash
vim motd.sh
```

You can write your commands inside this file. I'm not sure if `chmod` is necessary because there's no `sudo` but I still did it anyway.

```bash
chmod motd.sh 
```

