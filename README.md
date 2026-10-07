journalctl -u NetworkManager --since "2026-10-01" --no-pager | grep -i ens224
journalctl -k --since "2026-10-01" --no-pager | grep -i -E "ens224|vmxnet|link is"
dmesg -T | grep -i -E "ens224|vmxnet|link"
grep -i ens224 /var/log/messages | tail -50
