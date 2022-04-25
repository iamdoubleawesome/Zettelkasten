#24Mar2022

# How to add zsh for a user in docker?

1. Need to create a home folder for user first (optional)

   ```bash
   mkdir /home/alice
   ```

2. Copy all zsh files into this user's home folder
   ```bash
   cp -r /root/.oh-my-zsh ~alice
   ```

3. Change the ownership of the directory and all files inside this folder; use `-la` to see hidden files.
   ```bash
   cd alice
   chown alice:alice -R .
   chown alice:alice -R .*
   ls -la
   ```

   If not making this folder's ownership as user, it will have the warning when exec/exit the docker. Basically `zsh` is creating a `LOCK` file and it fails if user doesn't have the `write` right in the folder. 
   ```bash
   #exec
   zsh: locking failed for /home/alice/.zsh_history: permission denied: reading anyway
   #exit
   zsh: locking failed for /home/alice/.zsh_history: permission denied
   ```

4. Open `~/.zshrc` file and change the zsh `PATH` to this home folder via `nano`.

   ```bash
   nano ~/.zshrc
   ```

   and modify line 

   ```
   export ZSH="/home/alice/.oh-my-zsh"
   ```



### block

```bash
mkdir /home/alice
cp -r /root/.oh-my-zsh ~alice
cd alice
chown alice:alice -R .
chown alice:alice -R .*
ls -la
```

---

#zsh #docker

---

source: 

- @siargey
- https://github.com/ohmyzsh/ohmyzsh/issues/3512#issuecomment-694145825