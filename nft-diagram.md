# NFT

* NFT: Token with associated metadata

```                                                                                 
                                                                                                         
                                                                                                        
  ┌──────────────────┐                   ┌───────────────────────┐       ┌────────────┐  
  │     ACCOUNT      │      request      │       PROGRAM         │       │   Account  │
  │ The first user   ├──────────────────►│ The NFT Marketplace   │       │    Owner   │
  │                  │      to mint      │                       │       ├────────────┤
  ├──────────────────┤                   ├───────────────────────┤ ───►  │            │
  │ - Mints the NFT  │                   │- App you use to mint  │       │   Token    │  
  │ - Then, other    │                   │- An on-chain program  │ ───►  │            │
  │   accounts can   │                   │- Execute transactions │       │  Metadata  │  
  │   get the NFT    │                   │  for handling the NFT │       │            │  
  │   transfered to  │                   └───────────────────────┘       └────────────┘  
  │   them.          │                                                                                
  └──────────────────┘                                                                                
                                                                                                      
                                                                                                        
```                                                                              
                                                                                 
Minting
-------

* The Market place program use Solana's **SPL token** tooling to mint a new token and **set supply to 1**.
* Then it will freeze all minting of that token, as it should be unique and non-fungible.
* Program should implemnt the necessary logic to make only one token and associate to the respective metadata account.

