# fakedns

> Fake DNS server written in python 3

## What it does?

It responds to DNS `A` questions (host address questions), responding with the same IP over and over. The server is intended to be used when testing HTTP crawlers.

## Usage

Get information on your server's local IP address. Then set it as a nameserver in client's `/etc/resolv.conf` file (server can also be a client).
Assuming that your server's local IP is 192.168.1.5, client's `/etc/resolv.conf` file should look like this:

```
nameserver 192.168.1.5
```

Launch `fakedns.py` on server. It uses port 53, so you need to `sudo`. Assuming that you want to redirect all HTTP traffic to 192.168.1.6:

```shell
sudo python3 fakedns.py 192.168.1.6
```

## License

Copyright (c) 2014 Patryk Hes. Licensed under MIT license.
