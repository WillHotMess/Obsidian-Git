---
title: Untitled 1
desc: ""
---
sudo systemctl start containerd
sudo systemctl enable containerd   # start on boot
sudo systemctl status containerd   # verify it is running
kubectl get nodes -o wide
kubectl get nodes -l node-role.kubernetes.io/control-plane=""
# or on some distros:
kubectl get nodes -l node-role.kubernetes.io/master=""


sudo kubeadm token create --print-join-command
# 1. See if kubelet is even installed / has a unit
systemctl status kubelet

# 2. See if this node has kubeadm-style control-plane files
ls -R /etc/kubernetes

# 3. Check if containerd is running
systemctl status containerd
