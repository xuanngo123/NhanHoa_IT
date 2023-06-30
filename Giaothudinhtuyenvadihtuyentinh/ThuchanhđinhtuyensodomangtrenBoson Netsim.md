Thực hành định tuyến sơ đồ mạng trên Boson Netsim:

– Đầu tiên ta vào cấu hình IP cho 2 router

Tại Router0

Router>en

Router#conf t

Router(config)#hostname Router0

Router0(config)#interface f0/0

Router0(config-if)#ip address 10.0.0.1 255.255.255.0

Router0(config-if)#no shutdown

Router0(config-if)#exit

Router0(config)#interface f0/1

Router0(config-if)#ip address 192.168.1.1 255.255.255.0

Router0(config-if)#no shutdown

Tại Router1 

Router>en

Router#conf t

Router(config)#hostname Router1

Router0(config)#interface f0/0

Router0(config-if)#ip address 10.0.0.2 255.255.255.0

Router0(config-if)#no shutdown

Router0(config-if)#exit

Router0(config)#interface f0/1

Router0(config-if)#ip address 172.16.1.1 255.255.255.0

Router0(config-if)#no shutdown



– Để kích hoạt định tuyến tĩnh chúng ta có 2 cách cấu hình sau:

Cách 1:

Router(config)#ip route <Network\_đích> <Subnet Mask của Network\_đích> <IP 

nexthop>

Hoặc cách 2:

Router(config)#ip route <Network\_đích> <Subnet Mask của Network\_đích> <exit 

Interface>

Ví dụ ta với mô hình 

sau: 

Hình 1: Mô hình mạng sử dụng cấu hình Static

