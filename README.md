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


Java 8 Package
tar -xvf jdk-8u101-linux-i586.tar.gz
wget https://archive.apache.org/dist/hadoop/core/hadoop-2.7.3/hadoop-2.7.3.tar.gz
tar -xvf hadoop-2.7.3.tar.gz
vi .bashrc
source .bashrc
java -version
hadoop version
cd hadoop-2.7.3/etc/hadoop/
ls
vi core-site.xml
vi hdfs-site.xml
vi mapred-site.xml
vi yarn-site.xml
vi hadoop–env.sh
cd
cd hadoop-2.7.3
bin/hadoop namenode -format
cd hadoop-2.7.3/sbin
./start-all.sh
./hadoop-daemon.sh start namenode
./hadoop-daemon.sh start datanode
./yarn-daemon.sh start resourcemanager
./yarn-daemon.sh start nodemanager
./mr-jobhistory-daemon.sh start historyserver
jps
open the Mozilla localhost:50070/dfshealth.html check the NameNode interface.




