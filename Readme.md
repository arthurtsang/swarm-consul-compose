# setup

* replace node1/node2 to the ip address of docker swarm node in the cluster
* make sure docker daemon on node1/node2 is starts with -H 0.0.0.0:2375
* disable iptables/firewall

# to show all swarm nodes

docker -H tcp://node1:8888 run --rm swarm list consul://node1:8500/swarm

# to deploy container

docker -H tcp://node1:8888 run -d --name www -p 80:80 nginx

# to list running containers 

docker -H tcp://arthur-mesos-m1:8888 ps
