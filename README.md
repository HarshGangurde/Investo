# Investo

sudo apt update
sudo apt upgrade
egrep -c '(vmx|svm)' /proc/cpuinfo
kvm-ok
sudo apt install -y cpu-checker
sudo apt install -y qemu-kvm virt-manager libvirt-daemon-system virtinst libvirt-clients bridge-utils
sudo systemctl enable --now libvirtd
sudo systemctl start libvirtd
sudo systemctl status libvirtd
sudo usermod -aG kvm $USER
sudo usermod -aG libvirt $USER

cd /media
ls
mkdir guest_folder_name
sudo mkdir guest_folder_name
ls
sudo mount -t vboxsf host_fn G_fn


sudo apt update
sudo apt upgrade
sudo apt install docker.io
docker ––version
sudo systemctl enable docker
sudo systemctl start docker
sudo systemctl status docker
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add
sudo apt-add-repository "deb http://apt.kubernetes.io/kubernetes-xenial main"
sudo apt-get install kubeadm kubelet kubectl
sudo apt-mark hold kubeadm kubelet kubectl
kubeadm version
sudo swapoff –a
sudo hostnamectl set-hostname master-node
sudo hostnamectl set-hostname w1
sudo kubeadm init --pod-network-cidr=10.244.0.0/16
mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config
(sudo kubectl apply -f https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kube-flannel.yml)
kubectl get pods --all-namespaces
(kubeadm join --discovery-token abcdef.1234567890abcdef --discovery token-ca-cert-hash sha256:1234..cdef 1.2.3.4:6443)
kubectl get nodes

