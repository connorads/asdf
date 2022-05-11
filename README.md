# asdf

`asdf` is a CLI tool that can manage multiple language runtime versions on a per-project basis. It is like `gvm`, `nvm`, `rbenv` & `pyenv` (and more) all in one! Simply install your language's plugin!

## Tips

- `asdf` supports <kbd>tab</kbd> completion: If you don't remember a command, plugin name or which version(s) you have installed just press <kbd>tab</kbd>
![image](https://user-images.githubusercontent.com/10026538/152244355-d0636538-1c60-4d46-8978-e0b45831ff0b.png)
![image](https://user-images.githubusercontent.com/10026538/152244419-5b4198df-6435-4211-ac7c-9845c0571b08.png)
![image](https://user-images.githubusercontent.com/10026538/152244449-9d08d7b4-11d3-472a-bb23-83f2128048d4.png)

## Setup

Install asdf

`brew install asdf`

Create symlink to downloaded `.tool-versions` from default `.tool-versions` path

`ln -s ~/path/to/repo/asdf/.tool-versions ~/.tool-versions`

Install all tools defined in `.tool-versions`

`asdf install`

## Commands

List plugins

`asdf plugin list all`

Add plugins

```sh
asdf plugin add elixir
asdf plugin add erlang
asdf plugin add flutter
asdf plugin add golang
asdf plugin add nodejs
asdf plugin add ruby
```

List latest stable version

```sh
asdf latest nodejs 14
asdf latest nodejs 16
```

Install latest stable version

```sh
asdf install nodejs latest
asdf install nodejs latest 16
```

See current version

`asdf where nodejs`

Set current local version

`asdf local nodejs 12.22.4`

Set current global version

`asdf global nodejs 12.22.4`

Set current shell version

`asdf shell nodejs 12.22.4`

## Git

Ignore `.tool-versions` files globally

`echo ".tool-versions" > ~/.gitignore`

`git config --global core.excludesfile ~/.gitignore`
