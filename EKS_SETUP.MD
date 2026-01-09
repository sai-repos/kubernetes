#####   Version 0.221.0    #######

# Download and extract latest release
>  curl --silent --location "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_Linux_amd64.tar.gz" \
  | tar xz -C /tmp


# Move binary into your PATH
>  sudo mv /tmp/eksctl /usr/local/bin/

# Verify installation
>  eksctl version

 0.221.0