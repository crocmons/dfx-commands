### Deploy

Deploy

`dfx deploy --network ic`

https://smartcontracts.org/docs/developers-guide/cli-reference/dfx-deploy.html

Deploy actor with an arguments

https://smartcontracts.org/docs/candid-guide/candid-types.html

`dfx deploy --argument='()'`

`e.g. actor class Msg (message: Text) {}` - `dfx deploy --argument='("Msg")'`

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

Uninstall code

`dfx canister --network ic uninstall-code --all`

https://smartcontracts.org/docs/developers-guide/cli-reference/dfx-canister.html#_dfx_canister_call

### Wallet, Cycles, Identity

📚 https://internetcomputer.org/docs/current/developer-docs/build/project-setup/default-wallet/

Add a controller

`dfx wallet --network ic add-controller <controller-principal>`

List the current controllers

`dfx wallet --network ic controllers`

Remove a controller

`dfx wallet --network ic remove-controller <controller-principal>`

Add canister cycle wallet controller

https://forum.dfinity.org/t/if-a-cycles-wallet-creates-a-canister-via-the-cycles-wallet-web-ui-how-does-it-add-additional-controllers-to-those-anonymous-canisters/10544/7

`dfx canister --wallet CYCLES_WALLET_ID_THAT_IS_CONTROLLER --network ic call "CYCLE_WALLET_ID_THAT_WAS_CREATED_IN_UI" authorize '(principal "YOUR_PRINCIPAL_ID_FOR_DEVELOPER_IDENTITY_OR_NNS")'`

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

### Version Control

Downgrade DFX / Set particular DFX version

https://forum.dfinity.org/t/how-to-downgrade-dfx/13195

`DFX_VERSION=0.9.3 sh -ci "$(curl -fsSL https://smartcontracts.org/install.sh)"`

### Notes

null in `candid` == [] in `.js`

**@dfinity/principal**

Principal is not a string

To convert string to Principal:

`Principal.fromText(principalStr)`

e.g. `Principal.fromText(4i3qn-dmbtq-uqvxc-3un22-b6fp2-dzkgo-ocxrk-zmvvz-vqxno-rnjgd-zqe)`

To convert Principal to string:

`Principal.toText(principal)`

Principal methods:
.isAnonymous()
.toHex()
.toString()
.toText()
.toUint8Array()
