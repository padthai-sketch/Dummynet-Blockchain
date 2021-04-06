# Proof of Authority Development Chain - Dummynet

I developed a private testnet called 'Dummtnet' to explore potentials for blockchain by setting up the custom out-of-the-box blockchain using the Proof of Authority algorithm, and send a test transaction on MyCrypto application. 

Please see the following instructions on how to utilize these blocakchain tools.

**<ins>Setup your node accounts and custom testnest<ins>**

1. Innitiate with creating two nodes accounts for your network.
2. Using puppeth to build your new genesis block, name the network (in this case is 'Dummynet'), and choose 'Proof of Authority' as your consensus engine.
3. Included both Nodes addresses as your sealed account. Only included Node 1's address as your pre-funded account. 
4. Specify your chain/network ID then configured new genesis block to generate 'dummynet.json' as shown below.

***<p align="center">My Puppeth Configuration</p>***
<p align="center">
<img src="https://github.com/padthai-sketch/Dummynet-Blockchain/blob/main/Screenshots/Puppeth_Configuration.png" alt="Puppeth_Configuration" width="800"/>
</p>

**<ins>Initialize your node accounts<ins>**

1. With geth command, run Node 1 to unlock the account and begin mining process by running this command line<br> 
   *./geth --datadir node1 --unlock "SEALER_ONE_ADDRESS" --mine --miner.threads 1
2. Open the second tab for Node 2 to unlock the account, using this command line<br> 
   *./geth --datadir node2 --unlock "SEALER_TWO_ADDRESS" --port 30304 --rpc --bootnodes "enode://SEALER_ONE_ENODE_ADDRESS@127.0.0.1:30303" --allow-insecure-unlock
3. You should be able to see both nodes running at the same time. 

**<ins>Test your network on MyCrpto<ins>**

1. Login to your account on MyCrypto app to set up your custome network and connect the nodes with the exposed RPC port. 
2. After that send a transaction from the node1 account to the node2 account including the chain ID, and use ETH as the currency
3. Wait until TX status shows as 'Successful' and you're done!

***<p align="center">Transaction Metadata</p>***
<p align="center">
<img src="https://github.com/padthai-sketch/Dummynet-Blockchain/blob/main/Screenshots/TX_Status_successful.png" alt="TX_Status_successful" width="800"/>
</p>
