# Setting Up A Dev Environment

l like [Ubuntu](https://ubuntubudgie.org/downloads) as the best Linux distribution. Download (hands down) [the best operating system ever](https://ubuntubudgie.org/downloads) here.

Update the system:
```bash
sudo apt update && sudo apt upgrade -y
```

#### Install tools:
- [git](git.md)
- [gcc](gcc.md)
- [vim](vim.md)
- [openssh](ssh.md)

Always run `apt update` first before installing any software, else your Linux machine will turn into Windows and you'd be sorry. Just kidding. Actually, WIndows is a great OS, not just for games. Visual Studio is a great IDE for making a plethora of applications for all platforms and it can only be installed on a Windows device if I am not wrong.

```bash
sudo apt update && sudo apt upgrade -y
```

Then install the tools:

```bash
sudo apt install git gcc vim openssh
```

#### Configure the tools:
##### git
1. Set up a Git username:
```shell
git config --global user.name ""
```

2. Set an email address:
```shell
git config --global user.email ""
```
##### ssh
3. Next is to set up and configure `ssh` to be able to connect and push your codes to your Github repositories. This is also true when using Sublime Merge. Generating ssh keys on Working Copy is easier.

```bash
ssh-keygen -t ed25519 -C ""
```

4. Copy the contents in the generated `.pub` to your Github's SSH and GPG keys tab or section:
```bash
cat id_ed25519.pub
```

- [Github's documentation for generating SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=linux)

##### vim

Much of the changes I want to make for my toolbox could most probably be automated. I should learn how to do that someday.

For now, I'll just make a repository for all my config files so I can easily find them all in one place.

1. Create a `.gitignore` containing only `*`.
2. Initialize `home` and set up `git` repository.
```bash
cd ~
git init
git remote add origin git@github.com:knznsmn/dtfls.git
git fetch
git checkout -f main
```

Copied from this [page](https://drewdevault.com/2019/12/30/dotfiles.html).

Found this [page](https://dotfiles.github.io/). Should read this later.

##### bash
Make `bash` a lot prettier for eyescream experience using `oh-my-bash`.
```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"
```
#### Download other tools:

- [Vivaldi](https://vivaldi.com)
- [Station](https://github.com/getstation/desktop-app/releases)
- [Obsidian](https://www.obsidian.md)
	- [Markdown syntax](/sujets/cs/tables/md.md) 
- [Sublime Text](https://www.sublimetext.com/download_thanks?target=x64-deb)
	- [configurations](/outils/subl.md)
- [Sublime Merge](https://www.sublimemerge.com/download_thanks?target=x64-deb)
 
###### dotfiles
- .vimrc
- .bashrc

