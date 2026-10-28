
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo cat /proc/162545/wchan; echo
[sudo] senha para p585600:
ep_poll
[p585600@caddeapllx2651 ~]$ sudo ls -l /proc/162545/fd
total 0
lr-x------ 1 root root 64 out 28 13:56 0 -> 'pipe:[3517673]'
l-wx------ 1 root root 64 out 28 13:56 1 -> 'pipe:[3517674]'
l-wx------ 1 root root 64 out 28 13:56 2 -> 'pipe:[3517675]'
lrwx------ 1 root root 64 out 28 13:56 3 -> 'socket:[3516212]'
lr-x------ 1 root root 64 out 28 13:56 4 -> 'pipe:[3516221]'
lrwx------ 1 root root 64 out 28 13:56 5 -> 'anon_inode:[eventpoll]'
lr-x------ 1 root root 64 out 28 13:56 6 -> 'pipe:[3516222]'
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo ss -tnp | grep "pid=162545"
[p585600@caddeapllx2651 ~]$ sudo timeout 10 strace -p 162545 -s 200
timeout: falha ao executar o comando “strace”: Arquivo ou diretório inexistente
[p585600@caddeapllx2651 ~]$
