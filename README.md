# local-bin


```bash
VERSION="v0.0.1"
mkdir -p ~/.local/bin
curl -fSL "https://github.com/dyrnq/local-bin/archive/refs/tags/${VERSION}.tar.gz" | tar -xvz --directory=~/.local/bin --exclude=*.md --overwrite --strip-components=1
```


```bash
vi ~/.bashrc, append $HOME/.local/bin to $PATH.

if [ -d "$HOME/.local/bin" ] ; then
    PATH="$HOME/.local/bin:$PATH"
fi


```