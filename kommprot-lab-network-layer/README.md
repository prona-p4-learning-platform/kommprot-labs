# Simple intro to network host config, static routing and NAT


## Preparation

* add ip to host1:
  * ip addr add 192.168.188.100/24 dev eth1

* add ip to host2:
  * ip addr add 192.168.189.100/24 dev eth1


## Task 1: add routes to reach host1 from host2 and vice-versa

* host1:
  * ping 192.168.188.1 (test reachability of gateway...), arp -an?
  * ip route add 192.168.189.0/24 via 192.168.188.1

* host2:
  * ping 192.168.189.1
  * ip route add 192.168.188.0/24 via 192.168.189.1

### *To discuss*:
- solution folder? yes/no? full/partial solution?


## Task 2: add default route

* host1:
  * ip route 0.0.0.0/0 via 192.168.188.1

* host2:
  * ip route 0.0.0.0/0 via 192.168.189.1

*side note:* ...routes to 192.168.188.0/24 and 1921.68.189.0/24 can be removed now...

* add snat to router1:
  * iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE 


## Test: ping 192.168.188.100 <-> 192.168.189.100 ? -> 8.8.8.8, NetLab GW etc.?

- grading? bonus points? portfolio? partial grades/points? gradual feedback?
- network topo visualization in learn-sdn-hub?


## Extensions

- mtr, traceroute
- ipv6? (and other KommPro topics?)
- own subnetting?
