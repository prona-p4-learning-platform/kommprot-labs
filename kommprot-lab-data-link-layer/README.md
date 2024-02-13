# Prerequisites
- requires "sudo ovs-vsctl add-br switch1 || sudo ovs-vsctl add-br switch2 || sudo ovs-vsctl add-br switch3" to be run before the topology is started
- enable STP: "for NUMBER in $(seq 1 3); do sudo ovs-vsctl set bridge switch$NUMBER stp_enable=true; done"
- show stp state: "sudo ovs-appctl stp/show"

# Tasks?
- explore STP topology and blocked ports etc.? network topo visualization in learn-sdn-hub?

# Tests?

# Extensions?
- LLDP etc.? Features of OVS? (https://www.openvswitch.org/features/)
