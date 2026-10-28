sudo cat /proc/162545/wchan; echo
sudo ls -l /proc/162545/fd
sudo ss -tnp | grep "pid=162545"
sudo timeout 10 strace -p 162545 -s 200
