# Aleo Origin
Aleo Origin are gaming NFTs deployed on Aleo.

It has its origins in the belief in Aleo's privacy-preserving computing, and is a recognition of the contributions of all Aleo contributors, including (community users, developers, early investors in miners), etc.

Like the great physicists and astronomers in human history, they are constantly exploring and contributing to the progress of human civilization.

It is also a milestone in the development of Aleo. The birth of each planet is closely linked to the development of Aleo.

# Class
  Planets, moons, stars, black holes, escape cards, stealth cards, etc

Planet Legend - Important Milestone - Stellar Epic - Developer, Miner, Super Ambassador - Super Planet Rare - Community Ambassador - Planet Ordinary - Normal User - Satellite

Items: Black Hole Card, Escape Card, Stealth Card

All Mint funds will be staked into the ALEO mainnet POS, and the proceeds generated will be used for game rewards!!! We also offer free NFTs to mass players who only need to complete some very simple tasks

# First generation gameplay rules
    Players go to different kinds of planet NFTs and name them according to their own conditions. To form a complete galaxy, the composition of the galaxy needs to conform to the current basic laws of physics and astronomy to unlock Easter eggs Easter eggs have black hole cards, escape cards, stealth cards, detection cards. The black hole card can steal any celestial body whose energy is not 2 times larger than it, of course, the black hole cannot suck away the celestial body it wants to steal at a long distance, and each celestial body will appear in a position with space when it is born, and the player can choose by himself, because unreasonable entry will cause the galaxy body to be unstable, thus collapsing (destroying) Escape card: After being sucked away by the black body, it can be used to get returned. Stealth Card: Performs stealth effects within the effective time without being discovered by black holes. Probe card: Can detect the location of black holes. Each card can only be used once
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

```bash
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


