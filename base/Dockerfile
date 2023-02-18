FROM alpine

RUN apk add bash python3 vim tmux zsh curl git

RUN sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

WORKDIR /app

RUN curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim

COPY .vimrc .gitconfig .tmux.conf.local .tmux.conf /root/

RUN vim +PlugInstall +qall

