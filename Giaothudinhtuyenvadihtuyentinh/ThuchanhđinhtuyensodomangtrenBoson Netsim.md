Thực hành định tuyến sơ đồ mạng trên Boson Netsim:




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

ách 1: Router(config)#ip route <Network\_đích> <Subnet Mask của Network\_đích> <IP 

nexthop>

\+ Network: địa chỉ Network của các IP trong mạng (ví dụ trên network =172.16.1.0

\+ Nexthop: Là ip của cổng của Router kế tiếp trên đường đi tới network đích của packet

Tại Router0 , Network đích là 172.16.1.0 Subnet Mask 255.255.255.0; để sang được 

network này Router0 phải đi qua cổng F0/0 của Router1, mà cổng IP này có địa chỉ 

IP=10.0.0.1. Vậy cách 1 chúng ta có lệnh

Router0>en

Router0#conf t

Router0(config)#ip route  172.16.1.0 255.255.255.0 10.0.0.1

Tương tự như vậy trên Router1 muốn gửi packet tới network đích là 192.168.1.0 subnet 

mask 255.255.255.0 thì phải đi qua cổng nexthop là f0/0 của Router0 (mà IP của cổng 

này là 10.0.0.2)

Vậy trên Router1 ta có cấu hình:

Router1>en

Router1#conf t

Router1(config)#ip route 192.168.1.0 255.255.255.0 10.0.0.2

Note: Ta phải cấu hình trên tất cả các Router thì mới Ping thấy nhau vì gói tin phải được 

định tuyến đi và về (gửi và nhận)

Tại các PC ta đặt IP cho các máy theo thứ tự như hình 1

Cách 2: Router(config)#ip route <Network\_đích> <Subnet Mask của Network\_đích> 

<exit Interface>

\+ Exit Interface: Tên cổng thoát ra của Packet tại router được cấu hình ví dụ f0/0, s0/0

Trên Router0 muốn sang network đích thì gói tin sẽ được thoát ra từ cổng F0/0 chứ không 

phải f0/1 của Router này, nên ta có lệnh:

Router0(config)#ip route  172.16.1.0 255.255.255.0 f0/0

Tương tự ta có lệnh trên Router1:

Router0(config)#ip route  172.16.1.0 255.255.255.0 f0/0

Kết quả:

Với các PC và các cổng của Router đặt như trên hình ta có thể Ping từ PC0 tới 

tất cả các PC khác trong LAN


