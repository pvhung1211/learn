

Docker daemon (Docker engine) has a built-in DNS server that containers use by default

Static IP's and using IP's for talking to containers is an anti-pattern. Do your best to avoid it

Docker defaults the hostname (human-readable address of a container) to the container's name, but you can also set aliases