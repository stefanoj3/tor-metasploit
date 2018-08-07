### Tor + Metasploit docker-compose file

This repo contains a `docker-compose.yml` file that can be used to
quickly start to experiment with Metasploit through Tor SOCKS5.

Clone the repository, enter the folder and run:
```bash
docker-compose run --rm metasploit sh
```

Start mfsconsole:
```bash
./msfconsole
```

Verify what is your current external IP Address:
```
use gather/external_ip
run
```

Set the proxy and run it again, it should now be different.
```
set Proxies socks5:tor:9150
run
```

**WARNING**: this way you are always running the latest metasploit version