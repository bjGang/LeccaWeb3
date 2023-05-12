
## Download Node Binary
```
$ curl -sL https://api.github.com/repos/Joystream/joystream/releases/latest | jq -r ".tag_name"
```

Run as a Service
```
[Unit]
Description=Joystream Node
After=network.target

[Service]
Type=simple
User=joystream
WorkingDirectory=/home/joystream/bin/
ExecStart=/home/joystream/bin/joystream-node \
        --chain /home/joystream/bin/joy-mainnet.json \
        --pruning archive \
        --validator
Restart=on-failure
RestartSec=3
LimitNOFILE=10000

[Install]
WantedBy=multi-user.target
```
