# Reference Client overview

## General overview

Urbancash works through 2 separate binary files operated through command line:

1. **Urbancashd** – daemon to synchronize the blockchain and mine URBCcoins.
2. **simplewallet** – wallet to receive and send funds.

Make sure to place these files in one separate folder. 


## Install Urbancash

1. Unzip the archive to one separate folder. Urbancash will generate 
additional data files and log files in the same directory.
The blockchain data is stored in `~/.Urbancash` on Linux/Unix systems, 
`C:\Users\%USERNAME%\AppData\Roaming\Urbancash` on Windows or in
`~/Library/Application support/` on Mac OS.

## Launch Urbancash

1. Open **Urbancashd**

2. Wait until **Urbancashd** is synchronized. This may take a while. You will be 
notified with several green "SYNCHRONIZED OK" messages.

3. Open **simplewallet**.


## Daemon: synchronization and mining

After **Urbancashd** is launched you will have to wait until it is synchronized with 
the network. You will be notified with several green "SYNCHRONIZED OK" messages. 
Here are the most important daemon commands:

* `start_mining <wallet_address> [threads=1]` Start mining in several threads to a given wallet address
* `stop_mining`					Stop mining
* `show_hr`						Show current mining hashrate
* `hide_hr`						Stop showing current mining hashrate
* `help`						Show all daemon commands
* `exit`						Exit Urbancashd


## Wallet: send and receive payments

Simplewallet can only be used after the daemon is launched and synchronized. 
Simlewallet automatically synchronizes with Urbancashd. Here are the most 
important wallet commands:

* `address`						Show your wallet address
* `balance`						Show current wallet balance
* `transfer <mixin_count> <address> <amount>`	Send money to `<address>` with a mixing amount of `<mixin_count>`
* `start_mining <threads>`		Start mining in daemon with several threads to the current wallet address
* `stop_mining`					Stop mining in daemon
* `help`						Show all wallet commands
* `exit`						Exit simplewallet
