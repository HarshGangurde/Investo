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
