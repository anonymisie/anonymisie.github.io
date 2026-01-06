## start system container
```bash
docker run --rm -it -p 2137:2137 --name jekyll-dev ubuntu:jammy
```

## install jekyll
```bash
apt update && apt-get install ruby ruby-all-dev ruby-full build-essential zlib1g-dev ruby-dev build-essential make gcc -yy && echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc && echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc && echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc && source ~/.bashrc && gem install ffi jekyll bundler
```

## init site
```bash
mkdir site && cd site/ && jekyll new . && jekyll serve -H 0.0.0.0 -P 2137
```