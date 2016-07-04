# Base docker file

FROM fedora:latest

MAINTAINER gsiitbhu@gmail.com

    # Update
RUN dnf update -y && \
    # Install utilities 
    dnf install -y git vim zsh wget svn && \
    # Setup oh-my-zsh
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)" && \
    # Download my .vimrc
    wget https://gist.githubusercontent.com/mafiya69/eff689ff5030fa457d69f48f9dc19ae7/raw/32a6d3a9df88df2e111976dde2ba5ecef80cbbb3/.vimrc -O ~/.vimrc && \
    # Don't require sudo, already a root
    echo "alias sudo=" >> ~/.zshrc 

CMD ["/bin/zsh"]
