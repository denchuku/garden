
## Oh my zsh
"Oh my Zsh" is an extension to the zsh shell.

Url: [Oh My Zsh - a delightful & open source framework for Zsh](https://ohmyz.sh)

Your personal settings are located in file  `~/.zshrc`
Installation directory is `~/.oh-my-zsh`
	- If you want to override any of the default behaviors, just add a new file (ending in .zsh) in the custom/ directory, e.g. for aliases: `~/.oh-my-zsh/custom/aliases.zsh`

## Powerlevel10k theme
Url: [GitHub - romkatv/powerlevel10k: A Zsh theme](https://github.com/romkatv/powerlevel10k)

To configure call `p10k configure` and answer questions. This results in the settings to be saved in `~/.p10k.zsh`.

Install Meslo Nerd font ([GitHub - romkatv/powerlevel10k: A Zsh theme](https://github.com/romkatv/powerlevel10k#fonts)) and set font in your terminal app.

## JSON tools
[ohmyzsh/plugins/jsontools at master · ohmyzsh/ohmyzsh · GitHub](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/jsontools)

Pretty Print JSON:
```
$ echo '{"a":"foo","b":true}' | pp_json

{
    "a": "foo",
    "b": true
}
```