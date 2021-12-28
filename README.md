# What is Candle? (CNDL)

{% hint style="info" %}
**Good to know:** A succinct video overview is a great way to introduce folks to your product. Embed a Loom, Vimeo or YouTube video and you're good to go! We love this video from the fine folks at [Loom](https://loom.com) as a perfect example of a succinct feature overview.
{% endhint %}

### Protocol, Interface, Labs

To begin, we should make clear the distinctions between the different areas of "Candle", some of which may confuse new users.

* **Candle Labs**: The company which developed the Candle protocol, along with the web interface.
* **The Candle Protocol**: A suite of persistent, non-upgradable (for now - more on that later) smart contracts that together create an automated penance monetizer, a protocol that facilitates peer-to-peer charitable grant giving and making, using ERC-20 tokens on the Ethereum blockchain that users burn at their discretion.&#x20;
* **The Candle Interface**: A web interface that allows for easy interaction with the Candle protocol. The interface is only one of many ways one may interact with the Candle protocol.
* **Candle Governance**: A governance system for governing the Candle Protocol, enabled by the CNDL token. This will be live after a future upgrade.&#x20;

The following is a brief overview of the _Candle protocol_

### Introduction

The Candle protocol is a peer-to-peer\[^1] system designed for facilitating cryptocurrencies [(**ERC-20 Tokens**)](https://ethereum.org/en/developers/docs/standards/tokens/erc-20/) on the [**Ethereum**](https://ethereum.org) blockchain and the necessary human interaction required to execute the smart contract within the ecosystem. The protocol is implemented as a set of persistent, upgradable smart contracts; designed to prioritize censorship resistance, security, self-custody, and to function without any trusted intermediaries who may selectively restrict access.



### How does the Candle protocol compare to a typical Burning Contract?

To understand how the Candle protocol differs from a traditional burn, it is helpful to first look at two subjects: how the Candle design deviates from traditional burn order contracts, and how permissionless systems depart from conventional permissioned systems.

#### CNDL vs Others

Most publicly accessible tokens use a system where the user themselves are required to initiate a burning of tokens, done by sending them to a null address; also known as a "blackhole". After this is done, the tokens are irretrievable, thus reducing supply and theoretically increasing the price, though there are many other factors that affect this that are often overlooked. The users often submit their TX hash as proof, on a centralized medium such as twitter.&#x20;

The Candle protocol takes a different approach, using an Automated Burn Bin (ABB) in place of a null address and the related manual processes required to perform the burn.

At a very high level, an ABB allows a user to burn CNDL simply and easily with a few clicks, lets them choose the percent allocation that they wish to go to the Charitable Bin or the null address, and facilities governance functions for dispersing Charitable Bin funds.&#x20;

#### Permissionless Systems

When compared to traditional markets, the permissionless design of the Candle protocol stands out. Permissionless design means that the protocol’s services are entirely open for public use, with no ability to selectively restrict who can or cannot use them. Anyone can burn, vote, propose, develop, etc., at will. This is a departure from traditional financial services, which typically restrict access based on geography, wealth status, and age; or more related - traditional charitable / church-like services, which are lacking in transparency, ease of use and access, and are often corrupt.&#x20;

### Where can I find more information

For research into the theories of ABB, game theory, or optimization research, check out our [**research**](https://docs.uniswap.org/protocol/concepts/advanced/research) page.



\[^1] Ethereum protocols are sometimes referred to as peer-to-contract systems as well. These are similar to a peer-to-peer systems, but with immutable, persistent programs known as smart contracts taking the place of a peer.
