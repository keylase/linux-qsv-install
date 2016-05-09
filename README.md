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
5.
