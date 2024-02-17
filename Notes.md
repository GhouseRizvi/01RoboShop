Mongoedb should be running first then catlog should be running
then connect catalogue with mongo db then connect with web

### How to connect mongodb with catalogue??
Container should have proper names to connect with each other
if same name donesn't resolve the connection issue
try connecting via ip address, but there is a problem everytime container is created ip address may changed.

##### Docker Networking
dokcer network ls will give all the avaialable network
default network is bridge network.
default network cannot ressolve on name
so docker recommends to create our own bridge network.
ip a will give you all the avaialable network.

Network created by docker is called docker0
catalogue will get it ip from here 172.17.0.2 and mongod 172.17.0.3
similarly whenever a container is created container get its ip fron docker0 network pool, but it cause proble to connection between the containers.

so docker recommends to create own bridge network ro establish communication between the container nodes.

docker network create roboshop
this will create a private bridged network, the advantage here is we can isolate the containers which belongs to this network pool , from getting assigned to outerpools.
so other project will not get communicated with it, so this is safe
can comunicate using names in the network.


