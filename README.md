caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ df -h /tmp
Sist. Arq.                       Tam. Usado Disp. Uso% Montado em
/dev/mapper/VG_PRINCIPAL-LV_TMP  960M   50M  911M   6% /tmp
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ sudo lsof +L1 2>/dev/null | grep /tmp
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
