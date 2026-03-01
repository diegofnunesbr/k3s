# K3s

Este guia descreve a instalação e remoção do **K3s** em sistemas Linux, incluindo a criação automática de um cluster **Kubernetes** pronto para uso com o **kubectl**.

## Instalar o K3s

```bash
curl -sfL https://get.k3s.io | sh -s - --disable traefik --disable servicelb
mkdir -p ~/.kube
sudo cp /etc/rancher/k3s/k3s.yaml ~/.kube/config
sudo chown $USER:$USER ~/.kube/config
```

## Remover o K3s

```bash
sudo /usr/local/bin/k3s-uninstall.sh 2>/dev/null || true
sudo rm -rf ~/.kube
```
