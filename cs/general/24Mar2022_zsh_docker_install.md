#24Mar2022 

# How to install zsh by one line in docker?

```bash
sh -c "$(wget -O- https://github.com/deluan/zsh-in-docker/releases/download/v1.1.2/zsh-in-docker.sh)" -- \
```

change the theme of `zsh` via `nano`

```bash
nano ~/.zshrc
```

and modify line 

```
ZSH_THEME="cloud"
```



Could change user by following [this](24Mar2022_zsh_docker.md)

---

#zsh #docker

---

source: https://github.com/deluan/zsh-in-docker

