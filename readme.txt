How to setup?
1. Start the bitcoin daemon
1a. Ensure you are in 'btc-docker' directory. Type the following command (without quote) ==> "docker-compose up --build"
2. Start the bitcoin client to allow you to query the running bitcoin daemon
2a. Ensire you are in 'btc-client' directory. Type the following command (without quote) ==> "docker build -t bitcoincli ."
2b. Some useful command for btc-client (note, please change the rpcport to the right bitcoin daemon)
* docker run --net=host -it bitcoincli  -rpcport=18401 -regtest getbalance "*" 1 true
* docker run --net=host -it bitcoincli  -rpcport=18400 -regtest generate 101
* docker run --net=host -it bitcoincli  -rpcport=18402 -regtest getnewaddress
* docker run --net=host -it bitcoincli  -rpcport=18400 -regtest sendtoaddress "mjDaK78yWopz8TkC83PpUfXG7mBNYocMAo" 10
* docker run --net=host -it bitcoincli  -rpcport=18401 -regtest dumpprivkey "mjDaK78yWopz8TkC83PpUfXG7mBNYocMAo"
* docker run --net=host -it bitcoincli  -rpcport=18401 -regtest getbalance

Also worth looking at https://bitbucket.org/anxintl/anx-cold/src/dev/cold-utils/wallet/test/test-input-data.js
