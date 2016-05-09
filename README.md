# linux-qsv-install
info for step-by-step installation qsv on CentOS7.1

0. Install needed packages:
```
yum install -y mesa-dri-drivers
```
1.Download Intel Media Studio Community version:
```
http://registrationcenter-download.intel.com/akdlm/irc_nas/8684/MediaServerStudioEssentials2016.tar.gz
```
2.Unpack archive: 
```
tar xvzf MediaServerStudioEssentials2016.tar.gz && cd MediaServerStudioEssentials2016
```
3.Unpack SDK:
```
tar xvzf SDK2016Production16.4.4.tar.gz && cd SDK2016Production16.4.4/CentOS
```
4. Unpack install scripts:
```
tar xvzf install_scripts_centos_16.4.4-47109.tar.gz && ./install_sdk_UMD_CentOS.sh
```
5. install rpm:
```
rpm -Uvh --force drm-utils-2.4.56-47109.el7.x86_64.rpm libdrm-2.4.56-47109.el7.x86_64.rpm intel-linux-media-16.4.4-47109.el7.x86_64.rpm libva-1.67.0.pre1-47109.el7.x86_64.rpm intel-opencl-1.2-16.4-47109.el7.x86_64.rpm libva-utils-1.67.0.pre1-47109.el7.x86_64.rpm kernel-3.10.0-229.1.2.el7.src.rpm
```

#HINT multicast routing for Centos7:
```
firewall-cmd --permanent --direct --add-rule ipv4 filter INPUT 0 -m udp -p udp -m pkttype --pkt-type multicast -j ACCEPT
firewall-cmd --reload
```
