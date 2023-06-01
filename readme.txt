Тестовая лаба по Git'у
# Подсвечивание текущей ветки
mkdir ~/.bash
cd ~/.bash
git clone https://github.com/jimeh/git-aware-prompt.git
nano ~/.bashrc 
# and add the following to the bottom:
export GITAWAREPROMPT=~/.bash/git-aware-prompt
source "${GITAWAREPROMPT}/main.sh" 

export PS1="\${debian_chroot:+(\$debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\] \[$txtcyn\]\$git_branch\[$txtred\]\$git_dirty\[$txtrst\]\$ "
