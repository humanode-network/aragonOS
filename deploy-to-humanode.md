- Import private key to humanode network to `~/.aragon/humanode_key.json`

```
{
  "rpc": "http://127.0.0.1:9933",
  "keys": ["0x99b3c12287537e38c90a9219d4cb074a89a16e9cdb20bf85728ebd97c343e342"]
}
```

- Install deps

`yarn`

- Compile contracts

`yarn compile`

- A test humanode account with funds is used.

`OWNER="0x6Be02d1d3665660d22FF9624b7BE0551ee1Ac91b`

- Deploy ENS

`OWNER=0x6Be02d1d3665660d22FF9624b7BE0551ee1Ac91b npx truffle exec --network humanode scripts/deploy-test-ens.js`

- Deploy DaoFactory

`OWNER=0x6Be02d1d3665660d22FF9624b7BE0551ee1Ac91b npx truffle exec --network humanode scripts/deploy-daofactory.js`

- Deploy APM

`OWNER=0x6Be02d1d3665660d22FF9624b7BE0551ee1Ac91b ENS=<ENS Registry address>  DAO_FACTORY=<DAO Factory address from step 2> npx truffle exec --network <target network> scripts/deploy-apm.js`



