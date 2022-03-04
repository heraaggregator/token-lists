# Hera Tokenlists

Token Lists is a specification for lists of token metadata (e.g. address, decimals, etc.) that can be used by any dApp
interfaces that needs one or more lists of tokens. Anyone can create and maintain a token list, as long as they follow
the specification. The Hera community invites you to add your token to our tokenlists!


## Adding Your Token to an Existing List


### General Requirements
1. Token should be verified on the [andromeda explorer](https://andromeda-explorer.metis.io/).
2. Token must be added to a list that it qualifies for:
    * **[Hera Main Tokenlist](./heramain.tokenlist.json)**: Token must be in the Andromeda network!


## Adding Your Token
1. Add an entry in the `tokens` field of the appropriate tokenlist. Here is an example using WETH:
    ```json
    {
        "address": "0x420000000000000000000000000000000000000A",
        "chainId": 1088,
        "name": "Ether",
        "symbol": "WETH",
        "decimals": 18,
        "logoURI": "https://raw.githubusercontent.com/MetisProtocol/metis-bridge-resources/master/tokens/ETH/logo.png"
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

Netswap token logos are [hosted here](https://github.com/heraaggregator/tokens).
