  nmcli con mod "VMware customization ens224" ipv4.addresses 10.188.6.225/16
  nmcli con up "VMware customization ens224"

  arping -c3 -I ens224 10.188.0.16
ip neigh show dev ens224

