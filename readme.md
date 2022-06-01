### Deploy

Deploy

`dfx deploy --network ic`

https://smartcontracts.org/docs/developers-guide/cli-reference/dfx-deploy.html

Deploy actor with an arguments

https://smartcontracts.org/docs/candid-guide/candid-types.html

`dfx deploy --argument='()'`

`e.g. actor class Msg (message: Text) {}`

`dfx deploy --argument='("Text")'`

### Canister

Get canister id

`dfx canister id <CANISTER>`

Get canister id on the net

`dfx canister --network ic id <CANISTER>`

Call a specified method on a canister on the network

`dfx canister --network ic call <canister id> <method> [argument] [flag]`

`e.g. dfx canister --network ic call nbg4r-saaaa-aaaah-qap7a-cai getMinted --query`

Reinstall canister

`dfx canister --network ic install <canister name> -m reinstall`

https://smartcontracts.org/docs/developers-guide/cli-reference/dfx-canister.html#_dfx_canister_call

### Ledger / Wallet

Get ledger balance

`dfx ledger --network ic balance`

Check cycles balance

`dfx wallet --network ic balance`

Get wallet id

`dfx identity --network ic get-wallet`

Set wallet

`dfx identity --network=ic set-wallet <canister id>`

### Identity

Get current identity Principal

`dfx identity get-principal`

### Prices

Create new canister - 100 billion cycles - 100_000_000_000

https://smartcontracts.org/docs/developers-guide/computation-and-storage-costs.html

### Notes

**@dfinity/principal**

Principal is not a string

To convert string to Principal: `Principal.fromText(principalStr)`
e.g. `Principal.fromText(4i3qn-dmbtq-uqvxc-3un22-b6fp2-dzkgo-ocxrk-zmvvz-vqxno-rnjgd-zqe)`

To convert Principal to string: `Principal.toText(principal)`

Principal methods:
.isAnonymous()
.toHex()
.toString()
.toText()
.toUint8Array()
