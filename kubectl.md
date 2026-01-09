### KUBECTL 

>> curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"


-- Make the Binary Executable

>>  chmod +x kubectl

-- Move to a Directory in Your PATH

>> sudo mv kubectl /usr/local/bin/kubectl

-- Verify Installation

>> kubectl version --client

 o/p:   Client Version: v1.35.0
        Kustomize Version: v5.7.1