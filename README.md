# HeapZip blockchain in Rust
### Author : Dr. Mo Ashouri, ashourics@gmail.com 
### Contact: ashourics@protonmail.com
### Web: https://ashoury.net
### Twitter: https://twitter.com/ashourics
### YouTube: https://www.youtube.com/channel/UCp2VCfFn13kXwJd1HFBCa7Q


 A tutorial about how to build a blockchain in Rust

Start using

```bash
RUST_LOG=info cargo run
```

This starts the client locally. The blockchain is not persisted anywhere.

You can start it in multiple terminals to get multiple connected peer-to-peer clients.

In each client, you can enter the following commands:

* `ls p` - list peers
* `ls c` - print local chain
* `create b $data` - `$data` is just a string here - this creates (mines) a new block with the data entry `$data` and broadcasts it

Once a block is created by a node, it's broadcasted and the blockchain in all other nodes is updated (if it's a valid block).

On startup, a node asks another node on the network for their blockchain and, if it's valid and longer than the current local blockchain, it updates it's own chain to the longest one it receives.


Note that HeapZip Chain is a Basic Blockchain and needs further developments and security audits
