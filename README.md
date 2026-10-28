cat /sigdb/run

sudo mv /etc/init.d/sigdb /root/sigdb.initd.bkp

sudo tee /etc/systemd/system/sigdb.service >/dev/null <<'EOF'
[Unit]
Description=SIGDB Agent
After=network-online.target
Wants=network-online.target

[Service]
Type=simple
WorkingDirectory=/sigdb
ExecStart=/sigdb/run
Restart=on-failure
StandardOutput=journal
StandardError=journal

[Install]
WantedBy=multi-user.target
EOF

sudo systemctl daemon-reload
sudo pkill -f "./AgtSigdb -mtr7261lx651"     # derruba as 9 instâncias
sudo systemctl enable --now sigdb
ps -ef | grep -i [A]gtSigdb                  # deve sobrar 1

