# cni-ovs
This CNI plugin was created by LeanNet in order to further
popularize Open vSwitch based container cluster networking.

This simple pluging connect containers / pods directly to an
OVS bridge called br0, which eliminates the usage of any Linux Bridge,
and opens up the possiblities for high-level software defined networking.

Currenly we run the plugin as a native script on Kuberentes hosts.
Later releases will include Docker format.
But for now, in order to install do this::

    $ apt install -y openvswitch python3 python3-pip
    $ pip3 install netifaces
    $ cp lean_plugin /opt/cni/bin/lean_plugin
    $ cp etc/cni/net.d/mynet.conf /etc/cni/net.d/mynet.conf

Modify the mynet.conf file at every host in order to give IP addresses
from a different subnet!

Happy coding :-)

LeanNet
