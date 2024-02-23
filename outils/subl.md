# Sublime Text configuration

Sublime Text is awesome. With Terminus and a good theme, it's a very good text editor. Yes, VS Code has terminal built in but everybody knows that liking is wholly based on subjective parameters and we should just focus our logic inside the functions you make.

Now, to add a terminal to Sublime Text, install Terminus package.

1. `<Ctrl>` + `<Shift>` + `<P>` to open the command palette.
2. Install Package Control.
3. Install Terminus.
4. Restart Sublime Text.
5. Paste and save the following code to `Preferences` > `Package Settings` > `Terminus` > `Command Palette`:
```
[
   {
        "caption": "Terminal (panel)",
        "command": "terminus_open",
        "args"   : {
           "cmd": "bash",
           "cwd": "${file_path:${folder}}",
           "title": "Command Prompt",
           "panel_name": "Terminus"
        }
   },
]
```

6. To set `Alt + 1` to activate the terminal, paste and save the code below to `Preferences` > `Package Settings` > `Terminus` > `Key Bindings`:
```
[
   {
       "keys": ["alt+1"],
       "command": "terminus_open",
       "args" : {
           "cmd": "bash",
           "cwd": "${file_path:${folder}}",
           "panel_name": "Terminus"
       }
   }
]
```

Copied from this [tutorial](https://www.geeksforgeeks.org/how-to-use-terminal-in-sublime-text-editor/).
### Launching Sublime Text via Terminal

```bash
sudo ln -s /opt/sublime_text/sublime_text /usr/local/bin/subl
```
Copied from this [doc](https://www.sublimetext.com/docs/command_line.html).


#### Settings

```
{
	"theme": "Adaptive.sublime-theme",
	"font_size": 10,
	"font_face": "Jetbrains Mono",
	"save_on_focus_lost": true,
	"highlight_line": true,
	"caret_style": "phase",
	"ignored_packages":
	[],
}
```

Toggle focus between terminal and editor.
Check this issue out:
~~https://github.com/randy3k/Terminus/issues/302#issuecomment-1137223130~~

Just use `ctrl` + `'` for switch focus to editor and `alt` + `1` for switching focus to terminal. 

```
