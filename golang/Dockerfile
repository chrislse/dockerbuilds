FROM centos:latest
RUN echo 'starting' &&\
  yum install epel-release -y &&\
  yum install -y git \
  ctags \
  ruby-devel \
  rpm-build \
  python-devel ncurses-devel gettext perl-devel perl perl libacl-devel gpm-devel autoconf libselinux-devel desktop-file-utils gtk2-devel libSM-devel libXt-devel libXpm-devel perl-ExtUtils-Embed \
  gcc \
  bison \
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
  curl -s -S -L https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer| bash &&\
  source /root/.gvm/scripts/gvm &&\
  gvm install go1.4 &&\
  gvm use go1.4 &&\
  gvm install go1.6 &&\
  gvm use go1.6 --default
