# Aleo Origin

## Build Guide

To compile this Aleo program, run:
```bash
aleo build
```
## Example Usage

#### Initialize
The initialize function is used to load Arweave transaction ids into the global state. This global state acts to limit the number of total number of NFTs as well. If an Arweave transaction id, hasn't been upload, an NFT won't be able to mint it.

```bash
aleo run initialize 3u128 7u128
aleo run initialize 13u128 1u128
```

#### Premint
Since our unique minting mechanism requires an NFT to mint one, this method provides a way for a specific address to mint the root of the NFT minting tree.

```bash
aleo run premint aleo1y9mnptjc23wxtnr6gnjac0efu4fq859dsjk8mmryj3rg0feq0qzs8awmhn 3u128 7u128
```

```
>>>
```

```json
{
  owner: aleo1y9mnptjc23wxtnr6gnjac0efu4fq859dsjk8mmryj3rg0feq0qzs8awmhn.private,
  gates: 0u64.private,
  rank: 6u8.private,
  remaining: 3u8.private,
  data1: 3u128.private,
  data2: 7u128.private,
  _nonce: 2546588301349859963165576196445211638510724205660741519656114746669343010757group.public
}

```

#### Mint
Mint a new NFT to a new owner.
```bash
aleo run mint '{
  owner: aleo1y9mnptjc23wxtnr6gnjac0efu4fq859dsjk8mmryj3rg0feq0qzs8awmhn.private,
  gates: 0u64.private,
  rank: 6u8.private,
  remaining: 3u8.private,
  data1: 3u128.private,
  data2: 7u128.private,
  _nonce: 2546588301349859963165576196445211638510724205660741519656114746669343010757group.public
}' aleo17xy970uqxfjekll5zw6mtqz90pmsewe3u3a2lf4tg8mc0wpt3sqq3psxyt 13u128 1u128
```

#### Transfer
Transfer an NFT to a new owner.
```bash
aleo run transfer '{
  owner: aleo1y9mnptjc23wxtnr6gnjac0efu4fq859dsjk8mmryj3rg0feq0qzs8awmhn.private,
  gates: 0u64.private,
  rank: 6u8.private,
  remaining: 2u8.private,
  data1: 3u128.private,
  data2: 7u128.private,
  _nonce: 1700985124319758542136781077875397883667997810952789373247295650239946998473group.public
}' aleo17xy970uqxfjekll5zw6mtqz90pmsewe3u3a2lf4tg8mc0wpt3sqq3psxyt
```


