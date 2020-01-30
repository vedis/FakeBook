# FakeBook

## Uploading Files
### Rsync with Port
```rsync -va -e "ssh -p <port number>" <file> <user@server:directory>```

## Install Ruby
```brew install chruby automake bison openssl readline libyaml gdbm libffi```

Add to .zshrc:
```
source /usr/local/share/chruby/chruby.sh
source /usr/local/share/chruby/auto.sh
```

```
wget https://cache.ruby-lang.org/pub/ruby/2.4/ruby-2.4.0.tar.bz2
tar -xjvf ruby-2.4.0.tar.bz2
cd ruby-2.4.0
./configure --prefix="$HOME/.rubies/ruby-2.4.0" --with-opt-dir="$(brew --prefix openssl):$(brew --prefix readline):$(brew --prefix libyaml):$(brew --prefix gdbm):$(brew --prefix libffi)"
make
make install
```
