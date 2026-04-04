# local-bin


```bash
vi ~/.bashrc, append $HOME/.local/bin to $PATH.

if [ -d "$HOME/.local/bin" ] ; then
    PATH="$HOME/.local/bin:$PATH"
fi


```