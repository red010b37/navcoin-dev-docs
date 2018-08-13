---
date: 2018-04-16
title: "NavCoin Core Wallet Launch Options"
slug: navcore_launch_opt
url: /commands/navcore_launch_opt/
---
## NavCoin Core Wallet Launch Options


### Options

NavCoin Core version v4.3.0.0-cc3ca74-dirty (64-bit)
Usage:
  `navcoin-qt [command-line options]                     `

### Options:

```
-?
# Print this help message and exit 

-version
# Print version and exit 

-alertnotify=<cmd>
# Execute command when a relevant alert is received or we see a really long fork (%s in cmd is replaced by message) 

-blocknotify=<cmd>
# Execute command when the best block changes (%s in cmd is replaced by block hash) 

-bootstrap=<url>
# Specifies an URL from where a bootstrapped copy of the blockchain would be downloaded 

-checkblocks=<n>
# How many blocks to check at startup (default: 288, 0 = all) 

-checklevel=<n>
# How thorough the block verification of -checkblocks is (0-4, default: 3) 

-conf=<file>
# Specify configuration file (default: navcoin.conf) 

-datadir=<dir>
# Specify data directory 

-dbcache=<n>
# Set database cache size in megabytes (4 to 16384, default: 450) 

-loadblock=<file>
# Imports blocks from external blk000??.dat file on startup 

-maxorphantx=<n>
# Keep at most <n> unconnectable transactions in memory (default: 10) 

-maxmempool=<n>
# Keep the transaction memory pool below <n> megabytes (default: 50) 

-mempoolexpiry=<n>
# Do not keep transactions in the mempool longer than <n> hours (default: 72) 

-minersleep=<n>
# Sets the default sleep for the staking thread (default: 500) 

-mininputvalue=<n>
# Sets the minimum value for an output to be considered as a coinstake kernel candidate 

-par=<n>
# Set the number of script verification threads (-2 to 16, 0 = auto, <0 = leave that many cores free, default: 2) 

-pid=<file># 
# Specify pid file (default: navcoin.pid) 

-prune=<n>
# Reduce storage requirements by pruning (deleting) old blocks. This mode is incompatible with -txindex and -rescan. Warning: Reverting this setting requires re-downloading the entire blockchain. (default: 0 = disable pruning blocks, >550 = target size in MiB to use for block files) 

-reindex-chainstate
# Rebuild chain state from the currently indexed blocks 

-reindex
# Rebuild chain state and block index from the blk*.dat files on disk 

-staking=<bool>
# Enables or disables the staking thread. 

-sysperms
# Create new files with system default permissions, instead of umask 077 (only effective with disabled wallet functionality) 

-txindex
# Maintain a full transaction index, used by the getrawtransaction rpc call (default: 0) 

-addressindex
# Maintain a full address index, used to query for the balance, txids and unspent outputs for addresses (default: 0) 

-timestampindex
# Maintain a timestamp index for block hashes, used to query blocks hashes by a range of timestamps (default: 0) 

-spentindex
# Maintain a full spent index, used to query the spending txid and input index for an outpoint (default: 0) 
```

### Clock options:

```
-ntpserver=<ip/host>
# Adds a ntp server to use for clock syncronization 

-ntpminmeasures=<n>
# Min. number of valid requests to NTP servers (default: 3) 

-ntptimeout=<n>
# Number of seconds to wait for a response from a NTP server (default: 5) 

-maxtimeoffset=<n>
# Max number of seconds allowed as clock offset for a peer (default: 30) 
```

### Connection options:

```
-addnode=<ip>
# Add a node to connect to and attempt to keep the connection open 

-addanonserver=<ip>
# Add a NavTech node to use for private transactions 

-banscore=<n>
# Threshold for disconnecting misbehaving peers (default: 100) 

-bantime=<n>
# Number of seconds to keep misbehaving peers from reconnecting (default: 86400) 

-banversion=<string>
# Version of wallet to be banned 

-bind=<addr>
# Bind to given address and always listen on it. Use [host]:port notation for IPv6 

-connect=<ip>
# Connect only to the specified node(s) 

-devnet
# Uses the devnet network 

-discover
# Discover own IP addresses (default: 1 when listening and no -externalip or -proxy) 

-dns# 
# Allow DNS lookups for -addnode, -seednode and -connect (default: 1) 

-dnsseed
# Query for peer addresses via DNS lookup, if low on addresses (default: 1 unless -connect) 

-externalip=<ip>
# Specify your own public address 

-forcednsseed
# Always query for peer addresses via DNS lookup (default: 0) 

-listen
# Accept connections from outside (default: 1 if no -proxy or -connect) 

-listenonion
# Automatically create Tor hidden service (default: 1) 

-maxconnections=<n>
# Maintain at most <n> connections to peers (default: 125) 

-maxreceivebuffer=<n>
# Maximum per-connection receive buffer, <n>*1000 bytes (default: 5000) 

-maxsendbuffer=<n>
# Maximum per-connection send buffer, <n>*1000 bytes (default: 1000) 

-maxtimeadjustment
# Maximum allowed median peer time offset adjustment. Local perspective of time may be influenced by peers forward or backward by this amount. (default: 4200 seconds) 

-onion=<ip:port>
# Use separate SOCKS5 proxy to reach peers via Tor hidden services (default: -proxy) 

-onlynet=<net>
# Only connect to nodes in network <net> (ipv4, ipv6 or onion) 

-permitbaremultisig
# Relay non-P2SH multisig (default: 1) 

-peerbloomfilters
# Support filtering of blocks and transaction with bloom filters (default: 1) 

-port=<port>
# Listen for connections on <port> (default: 44440 or testnet: 15556 or devnet: 18886) 

-proxy=<ip:port>
# Connect through SOCKS5 proxy 

-proxyrandomize
# Randomize credentials for every proxy connection. This enables Tor stream isolation (default: 1) 

-requirednssec
# Requires DNS Sec for OpenAlias requests (default: true) 

-seednode=<ip>
# Connect to a node to retrieve peer addresses, and disconnect 

-stakervote=<string>
# Defines the staker vote to be attached to found blocks. 

-timeout=<n>
# Specify connection timeout in milliseconds (minimum: 1, default: 5000) 

-torcontrol=<ip>:<port>
# Tor control port to use if onion listening enabled (default: 127.0.0.1:9051) 

-torpassword=<pass>
# Tor control port password (default: empty) 

-upnp
# Use UPnP to map the listening port (default: 0) 

-whitebind=<addr>
# Bind to given address and whitelist peers connecting to it. Use [host]:port notation for IPv6 

-whitelist=<netmask>
# Whitelist peers connecting from the given netmask or IP address. Can be specified multiple times. Whitelisted peers cannot be DoS banned and their transactions are always relayed, even if they are already in the mempool, useful e.g. for a gateway 

-whitelistrelay
# Accept relayed transactions received from whitelisted peers even when not relaying transactions (default: 1) 

-whitelistforcerelay
# Force relay of transactions from whitelisted peers even they violate local relay policy (default: 1) 

-maxuploadtarget=<n>
# Tries to keep outbound traffic under the given target (in MiB per 24h), 0 = no limit (default: 0) 
```

### Wallet options:

```
-disablewallet
# Do not load the wallet and disable wallet RPC calls 

-keypool=<n>
# Set key pool size to <n> (default: 100) 

-fallbackfee=<amt>
# A fee rate (in NAV/kB) that will be used when fee estimation has insufficient data (default: 0.0002) 

-mintxfee=<amt>
# Fees (in NAV/kB) smaller than this are considered zero fee for transaction creation (default: 0.0001) 

-paytxfee=<amt>
# Fee (in NAV/kB) to add to transactions you send (default: 0.001) 

-rescan
# Rescan the block chain for missing wallet transactions on startup 

-salvagewallet
# Attempt to recover private keys from a corrupt wallet on startup 

-spendzeroconfchange
# Spend unconfirmed change when sending transactions (default: 1) 

-txconfirmtarget=<n>
# If paytxfee is not set, include enough fee so transactions begin confirmation on average within n blocks (default: 2) 

-usehd
# Use hierarchical deterministic key generation (HD) after BIP32. Only has effect during wallet creation/first start (default: 1) 

-upgradewallet
# Upgrade wallet to latest format on startup 

-wallet=<file>
# Specify wallet file (within data directory) (default: wallet.dat) 

-walletbroadcast
# Make the wallet broadcast transactions (default: 1) 

-walletnotify=<cmd>
# Execute command when a wallet transaction changes (%s in cmd is replaced by TxID) 

-zapwallettxes=<mode>
# Delete all wallet transactions and only recover those parts of the blockchain through -rescan on startup (1 = keep tx meta data e.g. account owner and payment request information, 2 = drop tx meta data) 
```

### ZeroMQ notification options:

```
-zmqpubhashblock=<address>
# Enable publish hash block in <address> 

-zmqpubhashtx=<address>
# Enable publish hash transaction in <address> 

-zmqpubrawblock=<address>
# Enable publish raw block in <address> 

-zmqpubrawtx=<address>
# Enable publish raw transaction in <address> 
```

### Debugging/Testing options:

```
-uacomment=<cmt>
# Append comment to the user agent string 

-debug=<category>
# Output debugging information (default: 0, supplying <category> is optional). If <category> is not supplied or if <category> = 1, output all debugging information.<category> can be: addrman, alert, bench, coindb, db, http, libevent, lock, mempool, mempoolrej, net, proxy, prune, rand, reindex, rpc, selectcoins, tor, zmq, qt. 

-help-debug
# Show all debugging options (usage: --help -help-debug) 

-logips
# Include IP addresses in debug output (default: 0) 

-logtimestamps
# Prepend debug output with timestamp (default: 1) 

-minrelaytxfee=<amt>
# Fees (in NAV/kB) smaller than this are considered zero fee for relaying, mining and transaction creation 

-maxtxfee=<amt>
# Maximum total fees (in NAV) to use in a single wallet transaction or raw transaction; setting this too low may abort large transactions 

-printtoconsole
# Send trace/debug info to console instead of debug.log file 

-shrinkdebugfile
# Shrink debug.log file on client startup (default: 1 when no -debug) 
```

### Chain selection options:

```
-testnet
# Use the test chain 

-devnet
# Use the dev chain

-regnet
# Use the regression chain
```

### Node relay options:

```
-bytespersigop
# Equivalent bytes per sigop in transactions for relay and mining (default: 20) 

-datacarrier
# Relay and mine data carrier transactions (default: 1) 

-datacarriersize
# Maximum size of data in data carrier transactions we relay and mine (default: 83) 

-mempoolreplacement
# Enable transaction replacement in the memory pool (default: 1) 
```

### Block creation options:

```
-blockmaxweight=<n>
# Set maximum BIP141 block weight (default: 3000000) 

-blockmaxsize=<n>
# Set maximum block size in bytes (default: 750000) 

-blockprioritysize=<n>
# Set maximum size of high-priority/low-fee transactions in bytes (default: 0) 
```

### RPC server options:

```
-server
# Accept command line and JSON-RPC commands 

-rest
# Accept public REST requests (default: 0) 

-rpcbind=<addr>
# Bind to given address to listen for JSON-RPC connections. Use [host]:port notation for IPv6. This option can be specified multiple times (default: bind to all interfaces) 

-rpccookiefile=<loc>
# Location of the auth cookie (default: data dir) 

-rpcuser=<user>
# Username for JSON-RPC connections 

-rpcpassword=<pw>
# Password for JSON-RPC connections 

-rpcauth=<userpw>
# Username and hashed password for JSON-RPC connections. The field <userpw> comes in the format: <USERNAME>:<SALT>$<HASH>. A canonical python script is included in share/rpcuser. This option can be specified multiple times 

-rpcport=<port>
# Listen for JSON-RPC connections on <port> (default: 44444 or testnet: 44445 or devnet: 44446) 

-rpcallowip=<ip>
# Allow JSON-RPC connections from specified source. Valid for <ip> are a single IP (e.g. 1.2.3.4), a network/netmask (e.g. 1.2.3.4/255.255.255.0) or a network/CIDR (e.g. 1.2.3.4/24). This option can be specified multiple times 

-rpcthreads=<n>
# Set the number of threads to service RPC calls (default: 4) 
```

### GUI options:

```
-updatefiatperiod=<miliseconds>
# Sets the interval in miliseconds to update the fiat price from CoinMarketcap. Min. 120000 
```

### UI Options:

```
-choosedatadir
# Choose data directory on startup (default: 0) 

-lang=<lang>
# Set language, for example "de_DE" (default: system locale) 

-min
# Start minimized 

-rootcertificates=<file>
# Set SSL root certificates for payment request (default: -system-) 

-splash 
# Show splash screen on startup (default: 1) 

-resetguisettings
# Reset all settings changed in the GUI 

