# local-bin


```bash
VERSION=$(curl -fsSL https://api.github.com/repos/dyrnq/local-bin/releases/latest | jq -r ".tag_name")
mkdir -p ~/.local/bin
curl -fSL "https://github.com/dyrnq/local-bin/archive/refs/tags/${VERSION}.tar.gz" | tar -xvz --directory=$(readlink -f ~/.local/bin) --exclude=*.md --overwrite --strip-components=1
```


```bash
vi ~/.bashrc, append $HOME/.local/bin to $PATH.

if [ -d "$HOME/.local/bin" ] ; then
    PATH="$HOME/.local/bin:$PATH"
fi


```