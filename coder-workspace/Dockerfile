
FROM codercom/enterprise-base:ubuntu

# Run everything as root
USER 0

# Install dependencies 
RUN DEBIAN_FRONTEND="noninteractive" apt-get update && apt-get install -y \
    curl \
    git \
    dirmngr \
    gpg \
    openssl \
    bzip2 \
    gawk \ 
    # python deps
    build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev

# Set back to coder user
USER 1000
WORKDIR /home/coder
    # Add asdf plugins (alphabetical)
    # Install a version of each tool (latest by default)
    # Set the tool-version of each
    # AWS CLI
# Setup asdf
RUN git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.9.0 && \
    echo "source $HOME/.asdf/asdf.sh" >> ~/.bashrc && \
    echo "source $HOME/.asdf/completions/asdf.bash" >> ~/.bashrc && \
    source $HOME/.asdf/asdf.sh && \
    # Need to fix directory permissions for plugin folders
    asdf plugin add python && \
    asdf install python latest && \
    asdf global python latest && \
    asdf plugin add awscli && \
    asdf install awscli latest && \
    asdf global awscli latest && \
    asdf plugin add direnv && \
    asdf install direnv latest && \
    asdf global direnv latest && \
    asdf plugin add eksctl && \
    asdf install eksctl latest && \
    asdf global eksctl latest && \
    asdf plugin add flux2 && \
    asdf install flux2 latest && \
    asdf global flux2 latest && \
    asdf plugin add gcloud && \
    asdf install gcloud latest && \
    asdf global gcloud latest && \
    asdf plugin add helm && \
    asdf install helm latest && \
    asdf global helm latest && \
    asdf plugin add helm-diff && \
    asdf install helm-diff latest && \
    asdf global helm-diff latest && \
    asdf plugin add helmfile && \
    asdf install helmfile latest && \
    asdf global helmfile latest && \
    asdf plugin add kubectl && \
    asdf install kubectl latest && \
    asdf global kubectl latest && \
    asdf plugin add kustomize && \
    asdf install kustomize latest && \
    asdf global kustomize latest && \
    asdf plugin add nodejs && \
    asdf install nodejs latest && \
    asdf global nodejs latest && \
    asdf plugin add pulumi && \
    asdf install pulumi latest && \
    asdf global pulumi latest && \
    asdf plugin add sops && \
    asdf install sops latest && \
    asdf global sops latest && \
    asdf plugin add terraform && \
    asdf install terraform latest && \
    asdf global terraform latest && \
    asdf plugin add terraform-docs && \
    asdf install terraform-docs latest && \
    asdf global terraform-docs latest
