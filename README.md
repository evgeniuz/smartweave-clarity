# Port of SmartWeave Hello World contract (https://github.com/ArweaveTeam/SmartWeave/blob/master/CONTRACT-GUIDE.md) to Clarity

## Usage:

### Deploy contract
```
smartweave-cli --key-file <keyfile.json> --create --contract-src contract.js --init-state init-state.json
```

### Check state, should have all flags set to `false`
```
smartweave-cli --key-file <keyfile.json> --contract <contract-tx-id> --get-state
```

### Send "hello"
```
smartweave-cli --key-file <keyfile.json> --interact --contract <contract-tx-id> --input-file call-hello.json
```

### Check state, should have only heardHello as `true`

### Send "world"
```
smartweave-cli --key-file <keyfile.json> --interact --contract <contract-tx-id> --input-file call-world.json
```

### Check state, should have all flags set to `true`