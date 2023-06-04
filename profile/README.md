# VeriSocial - Verifiable Social Hub for Content Creators

VeriSocial is a place where anyone can verify their social media on-chain. This platform aims to allow anyone to have their social media verified, allowing any social media companies to authenticate their users through ease of integration.

## Technology Stack

- Frontend: React and Next.js
- Backend: Node.js
- Smart Contracts: Solidity
- GraphQL APIs: Custom Subgraphs with The Graph
- Authentication: OAuth (GitHub, WorldID)
- IPFS Storage: Client Library
- Database: Prisma, Supabase

## How it Works

### User Authentication

Users log in to their social media accounts with OAuth (Github, Twitter) or using OTP verification on messaging platforms (Telegram, Line)

### User Registration

Users are minted a social proof ERC-721 token when they create their profile for the first time. If a user isn't registered yet, they will not have an ERC-721. Each user can only have one ERC-721.

### Store the CID on-chain

A MetaMask transaction is triggered to store the CID in the respective smart contract depending on the module (GitHub, WorldID, Telegram), associating it with the user's Ethereum address. An ERC-721 token is minted for the user. This ERC-721 will enable other platforms to build on top of the dApp since all social media information is stored inside it.
### User Profile

Anyone is able to view the full list of Social Media channels that the person has claimed

