# K3s

### Instalar o K3s

- `git clone https://github.com/diegofnunesbr/k3s.git`
- `cd k3s`
- `curl -sfL https://get.k3s.io | sh -s - --disable traefik --disable servicelb --write-kubeconfig-mode 644`
- `mkdir -p ~/.kube`
- `cp /etc/rancher/k3s/k3s.yaml ~/.kube/config`
- `chown $USER:$USER ~/.kube/config`
