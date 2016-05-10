FROM centos:latest

RUN yum install epel-release -y &&\
  yum -y install nodejs \
  npm \
  git \
  ctags \
  ruby-devel \
  rpm-build \
  python-devel ncurses-devel gettext perl-devel perl perl libacl-devel gpm-devel autoconf libselinux-devel desktop-file-utils gtk2-devel libSM-devel libXt-devel libXpm-devel perl-ExtUtils-Embed \
  gcc \
  openssl \
  wget \
  vim &&\
  mkdir -p ~/.vim/autoload ~/.vim/bundle && \
  curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim &&\
  cd ~ &&\
  git clone https://github.com/chrislse/prepare-vim-dev-env &&\
  cd prepare-vim-dev-env &&\
  ruby install.rb &&\
  cp .vimrc ~/ &&\
  echo 'alias vi="/usr/bin/vim"' >> ~/.bashrc &&\
  npm install -g express-generator
