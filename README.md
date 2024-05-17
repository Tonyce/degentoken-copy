# CopyDegenToken

## Deployed Contracts

```bash
❯ forge create --rpc-url https://base-sepolia.g.alchemy.com/v2/mwGPVe9op8x1I6WTVgDo2qjRbbEmQbSV \                                                                                                    ─╯
   --constructor-args 1716052050 \
  --private-key $PRIVATE_KEY \
  src/DegenCopy.sol:DegenCopyToken
[⠆] Compiling...
No files changed, compilation skipped
Deployer: 0x3ae6c93C96e0366b899bEe8e286a6946a9DAd52b
Deployed to: 0xD084FD38BB7fDba38b0a2BffbA9e558ce29Ad8AC
Transaction hash: 0x6dc27da20a3ba679a30325f319c8fd0801516660e2905df0c044f2d1616d57b9

```

## Verify Contracts

```bash
❯ forge verify-contract --chain-id 84532 \                                                                                                                                                           ─╯
  --watch \
  --etherscan-api-key $ETHERSCAN_API_KEY \
  0xD084FD38BB7fDba38b0a2BffbA9e558ce29Ad8AC \
  src/DegenCopy.sol:DegenCopyToken --constructor-args $(cast abi-encode "constructor(uint256)" 1716052050) 
Start verifying contract `0xD084FD38BB7fDba38b0a2BffbA9e558ce29Ad8AC` deployed on base-sepolia

Submitting verification for [src/DegenCopy.sol:DegenCopyToken] 0xD084FD38BB7fDba38b0a2BffbA9e558ce29Ad8AC.
Submitted contract for verification:
        Response: `OK`
        GUID: `rygez9uaj39zmjvl8bupt5npkzuuzfebxdyrjsmdzzu3na8bfp`
        URL: https://sepolia.basescan.org/address/0xd084fd38bb7fdba38b0a2bffba9e558ce29ad8ac
Contract verification status:
Response: `NOTOK`
Details: `Pending in queue`
Contract verification status:
Response: `OK`
Details: `Pass - Verified`
Contract successfully verified
```