# Hera Dex Aggregator - Tokenlists

### Active Tokenlists

1. **Metis:** [heramain-v2.tokenlist.json](./heramain-v2.tokenlist.json)

### Pending Tokenlists

1. **Arbitrum:** [herav2-arbitrum-maintokens.json](./herav2-arbitrum-maintokens.json)

Token Lists is a specification for lists of token metadata (e.g. address, decimals, etc.) that can be used by any dApp
interfaces that needs one or more lists of tokens. Anyone can create and maintain a token list, as long as they follow
the specification. The Hera community invites you to add your token to our tokenlists!


## Adding Your Token to an Existing List


### General Requirements
1. Token should be verified on token explorers.
2. Token must be added to a list that it qualifies for:
    * **[Hera Main Tokenlist - Metis](./heramain-v2.tokenlist.json)**: Token must be in the Andromeda network!
    * **[Hera Arbitrum Main Tokens - Metis](./herav2-arbitrum-maintokens.json)**: Token must be in the Arbitrum chain!


## Adding Your Token
1. Add an entry in the `tokens` field of the appropriate tokenlist. Here is an example using WETH:
    ```json
    {
        "address": "0x420000000000000000000000000000000000000A", // Token contract address
        "chainId": 1088, //ChainID
        "name": "Ether",
        "symbol": "WETH",
        "decimals": 18,
        "logoURI": "https://raw.githubusercontent.com/heraaggregator/arbitrum-tokens/main/0xeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee.png" // Logo URL
    }
    ```
2. Update the `timestamp` field to the current timestamp.
3. Update the `version` field to adhere to semantic versioning:

    * Increment major version when tokens are removed
    * Increment minor version when tokens are added
    * Increment patch version when tokens already on the list have minor details changed (name, symbol, logo URL, decimals)

    ***Note:*** Changing a token address or chain ID is considered both a remove and an add, and should be a major version update.


## Creating Your Own List

List creation is encouraged! The Hera team wants the community to develop their own lists and will not gatekeep new lists.


## Adding Your Token Logo

* Token logos are [hosted here](https://github.com/heraaggregator/tokens) for Metis side.
* Token logos are [hosted here](https://github.com/heraaggregator/arbitrum-tokens) for Arbitrum side.
