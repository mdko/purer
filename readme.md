# Purer

> Pretty one-line ZSH prompt based on [@DFurnes](https://github.com/DFurnes)'s [Purer](https://github.com/DFurnes/purer) fork of [@sindresorhus](https://github.com/sindresorhus/)'s [Pure](https://github.com/sindresorhus/pure)

![purer](https://cloud.githubusercontent.com/assets/583202/25418314/c3a29bfa-2a18-11e7-8a6f-4c0960ccadfc.png)

## The Difference

Right now, the only difference between this and Pure(r) is that I add the iTerm2 prompt mark to the appropriate place in the prompt,
so that moving between prompts in iTerm2 via Cmd-Shift-Up and Cmd-Shift-Down works properly.

**Important**: Note that because of loading order issues, for this to work, you need to move the shell integration line you probably currently
have in your `~/.zshrc` instead to your `~/.zshenv` so that it doesn't complain whenever you load the prompt.

```sh
  file source ~/.iterm2_shell_integration.zsh
```

Otherwise, you'll see the error: `prompt_pure_preprompt_render:27: command not found: iterm2_prompt_mark` everytime you load the prompt.

## Install

Can be installed with `npm` or [manually](https://github.com/sindresorhus/pure/blob/master/readme.md#manually). Requires Git 2.0.0+ and ZSH 5.2+.

```sh
$ npm install --global purer-prompt
```

Initialize the prompt system (if not so already) and choose `purer`:

```sh
# .zshrc
autoload -U promptinit; promptinit
prompt purer
```

See [Pure's readme](https://github.com/sindresorhus/pure/blob/master/readme.md#install) for more detailed instructions.

## Customization

Purer supports customization using [Pure's environment variables](https://github.com/sindresorhus/pure#options), plus:

### `PURE_PROMPT_SYMBOL_COLOR`

Defines the prompt symbol color. The default value is `magenta`; you can use any [colour name](https://wiki.archlinux.org/index.php/Zsh#Colors) or [numeric colour code](https://upload.wikimedia.org/wikipedia/commons/1/15/Xterm_256color_chart.svg) (see `zshzle(1)` section [Character Highlighting](http://zsh.sourceforge.net/Doc/Release/Zsh-Line-Editor.html#Character-Highlighting).)

## License

Purer MIT © [David Furnes](http://dfurnes.com) <br/>
Pure MIT © [Sindre Sorhus](http://sindresorhus.com)
