* Install mycrypto

* Create two node accounts

```
./geth account new --datadir node 1
```

```
--datadir node1 # specify location of new node
```
* Choose password to seal wallet
* Run puppeth

```
./puppeth
```
* Select properties of network
	* Block time - Speed at which blocks can be created
	* Chose Clique (Proof of Authority) - Method of which nodes agree upon transactions
	* Chain ID - Unique identifier for the network

	* Pre-fund your node accounts

* Export network and copy to directory containing nodes, and view it
[!image][Screenshots/img1.PNG]

* Initialize nodes with geth and network
```
./geth init mynetwork.json --datadir node1/
```
* Run your nodes
```
./geth --datadir node1 --port 30304 --rpc --mine --minerthreads 1
```
```
--port 30304 # specify port to avoid conflicts
```
```
---rpc # allow outside connections to the node
```
```
--mine # tell the node to begin mining
```
```
--minerthreads 1 # number of cpu threads assigned to the node
``` 
```
./geth --datadir 2 --mine --minerthreads 1 --bootnodes "encode://fromNode1"
```
```
--bootnodes # nodes to connect to upon running
```

* From mycrypto create a new node
[!image][Screenshots/img2.PNG]
* Log in via keystore file
[!image][Screenshots/img3]
* Send transaction by inputing other nodes address
[!image][Screenshots/img4]
* Check on transaction status
[!image][Screenshots/img5]

