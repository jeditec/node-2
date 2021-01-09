# node-2

This is the configuration for node-2 of VPN proxy implementation with google cloud.

For apps running on non standard 443 port we can use.

In this example we will redirect from port 443 to port 8006.

/sbin/iptables -F

/sbin/iptables -t nat -F

/sbin/iptables -t nat -A PREROUTING -p tcp --dport 443 -j REDIRECT --to-ports 8006
