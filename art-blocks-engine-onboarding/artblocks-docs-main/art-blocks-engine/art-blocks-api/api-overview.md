# API Overview

An overview of the current Art Blocks APIs.

!!!
We are currently in the process of working on finalizing a more comprehensive project-oriented API which we plan to release in the first half of 2022. This API will encapsulate both onchain data (the information readily available via the Art Blocks public subgraph on The Graph) and additional off-chain data (e.g., all available features for a given project)
!!!

Quick Links:
- [Token API](#token-api)
- [Generator API](#generator-api)
- [Media API/Media Server](#media-apimedia-server)
- [Art Blocks Subgraph](#art-blocks-subgraph)

## Hosted APIs

As a quick overview, the main APIs that exist currently are:

<br>

### Token API

Provides the token metadata for a given Art Blocks token.

**Mainnet**

* Note: Contract address is required for Engine

| Contract Type | Pattern | Sample |
| --- | --- | --- |
| Engine |  `https:token.artblocks.io/{contractAddress}/{tokenID}` | https://token.artblocks.io/0x0a1bbd57033f57e7b6743621b79fcb9eb2ce3676/110000 |


**Testnet**

| Contract Type | Pattern | Sample |
| --- | --- | --- |
| Engine | `https:token.staging.artblocks.io/{contractAddress}/{tokenID}` | https://token.staging.artblocks.io/0x81236b5a105d3ad6b56ac41a03e1fd8893a08859/1000001 |


<br>

### Generator API

Provides an i-frame-able live-view for the art associated with a given Art Blocks Engine token.

**Mainnet**

* Note: Contract address is required for Engine

| Contract Type | Pattern | Sample |
| --- | --- | --- |
| Engine | `https://generator.artblocks.io/{contractAddress}/{tokenID}` | https://generator.artblocks.io/0x0a1bbd57033f57e7b6743621b79fcb9eb2ce3676/11000083 |

**Testnet**

| Contract Type | Pattern | Sample |
| --- | --- | --- |
| Engine | `https://generator-staging-goerli.artblocks.io/{contractAddress}/{tokenID}` | https://generator-staging-goerli.artblocks.io/0xe745243b82ebc46e5c23d9b1b968612c65d45f3d/1000001 |

<br>

### Media API/Media server

Provides a static snapshot of the rendered live-view for a given Art Blocks Engine token.

**Mainnet**

Currently, media is accessible through individual s3 buckets.

| Render Type | Pattern | Sample |
| --- | --- | --- |
| Standard | `https://{enginePartner}-mainnet.s3.amazonaws.com/{tokenID}.png` | https://bright-moments-mainnet.s3.amazonaws.com/8000000.png |
| Thumbnail | `https://{enginePartner}-mainnet.s3.amazonaws.com/thumb/{tokenID}.png` | https://bright-moments-mainnet.s3.amazonaws.com/thumb/8000000.png |

**Testnet**

| Contract Type | Render Type | Pattern | Sample |
| --- | --- | --- | --- |
| Engine | Standard | `https://{enginePartner}-goerli.s3.amazonaws.com/{tokenID}.png` | https://bright-moments-goerli.s3.amazonaws.com/1000000.png |

Please also note that the Generator API and Media API links for a given token are included in the token response for that token from the Token API.

## Art Blocks Engine Subgraph

Art Blocks has a GraphQL API Endpoint hosted by [The Graph](https://thegraph.com/docs/about/introduction#what-the-graph-is) called a subgraph for indexing and organizing data from the Art Blocks Engine smart contracts.

This subgraph can be used to query for on-chain data related to the Art Blocks Engine contracts.

Subgraph information is serviced by a decentralized group of server operators called Indexers.

## Ethereum Mainnet

- [Explorer Page](https://thegraph.com/explorer/subgraph?id=5So3nipgHT3ks7pEPDQ6YgSFhfEmADrh481P9z1ZtcMA&view=Overview)
- Graphql Endpoint: https://api.thegraph.com/subgraphs/name/yyd01245/artblocks
- [Code Repo](https://github.com/ArtBlocks/artblocks-subgraph)

## Helpful Resources

- [Video Tutorial on creating an API Key](https://www.youtube.com/watch?v=UrfIpm-Vlgs)
- [Managing your API Key & setting your indexer preferences](https://thegraph.com/docs/en/studio/managing-api-keys/)
- [Querying from an application](https://thegraph.com/docs/en/developer/querying-from-your-app/)
- [How to use the explorer and playground to query on-chain data](https://medium.com/@chidubem_/how-to-query-on-chain-data-with-the-graph-f8507488215)


## The Art Blocks Engine mainnet subgraph can currently be queried a few ways:

| The Graph Service           | Art Blocks Data | Limited Secondary Sales Data | URL                                                                                    |
| --------------------------- | --------------- | ---------------------------- | -------------------------------------------------------------------------------------- |
| Hosted Service              | Yes             | No                           | https://thegraph.com/hosted-service/subgraph/artblocks/art-blocks                      |
| Hosted Service              | Yes             | Yes^[1]                      | https://thegraph.com/hosted-service/subgraph/artblocks/art-blocks-with-secondary       |
| Decentralized Graph Network | Yes             | No                           | https://thegraph.com/explorer/subgraph?id=0x3c3cab03c83e48e2e773ef5fc86f52ad2b15a5b0-0 |

> [1] Currently limited to OpenSea & LooksRare

<br>

The Art Blocks testnet subgraph can be queried at the URL below:

| The Graph Service | Art Blocks Data | URL |
| --- | --- | --- |
| Hosted Service | Yes | https://thegraph.com/hosted-service/subgraph/artblocks/art-blocks-artist-staging-goerli |

**Recommendation:** Using the above links, familiarize yourself with the subgraph’s schema, via the GraphQL playground.
