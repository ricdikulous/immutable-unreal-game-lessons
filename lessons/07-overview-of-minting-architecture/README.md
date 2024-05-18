# 07 - Overview of Minting Architecture

## Introduction

In this lesson, we will explore the architecture required to add NFT minting functionality to our game. The focus will be on understanding the overall architecture without diving into code, providing a clear picture of how minting will be integrated.

## Lesson Objective

By the end of this lesson, you will have a clear understanding of the overall architecture for minting NFTs within our game, including how to expand the current integration with the Immutable Passport to enable NFT minting and usage in the game.

## Overview

1. **Current State and Goals**: Overview of the current game setup and the desired end state.
2. **Architecture Overview**: Detailed explanation of the architecture for NFT minting.
3. **Components and Interactions**: Description of the main components involved and their interactions.
4. **Implementation Plan**: Steps required to implement the architecture.

## Prerequisites

Before starting this lesson, ensure you have completed the previous lesson on [Retrieve Player Data with Immutable Passport](../05-retrieve-player-data-with-immutable-passport/README.md), which covers fetching player wallet information and NFTs.

## Step-by-Step Instructions

### Current State and Goals

**Current State**:
- Basic integration with Immutable Passport allows players to log in and fetch basic details.
- Players can view their NFTs on a placeholder screen.
- Character select screen only allows selection of a default character.
- NFT minting screen is present but non-functional.

**End Goals**:
- Display player's NFTs in the inventory with details and traits.
- List NFTs as selectable playable characters.
- Enable NFT minting upon completing specific in-game tasks.

### Architecture Overview

To integrate NFT minting, we will need to expand our architecture to include:

- **Immutable Passport Integration**: For player login and data retrieval.
- **Minting Server**: A dedicated server responsible for minting NFTs.
- **S3 Bucket**: For storing NFT metadata.
- **Game Integration**: Updated game logic to interact with the minting server and display NFTs.

### Components and Interactions

1. **Game**:
   - Requests NFT minting upon specific conditions.
   - Displays NFTs in the inventory and character select screen.
   
2. **Minting Server**:
   - Receives minting requests from the game.
   - Uploads NFT metadata to the S3 bucket.
   - Initiates minting process using the Immutable SDK.
   - Returns minted NFT metadata to the game.

3. **S3 Bucket**:
   - Stores NFT metadata.
   - Provides access to NFT images for display in the game.

4. **Immutable SDK**:
   - Facilitates player login and data retrieval.
   - Handles NFT minting process.

### Implementation Plan

**Step 1**: Set up AWS S3 for storing NFT metadata.  
**Step 2**: Develop and deploy a minting server locally (for educational purposes).  
**Step 3**: Update the game to request NFT minting from the server.  
**Step 4**: Ensure the game fetches and displays NFT metadata and images from the S3 bucket.

## Conclusion

In this lesson, we covered the overall architecture required to integrate NFT minting into our game. We outlined the current state, the desired end goals, and the components involved in the architecture. This sets the stage for implementing the minting functionality in the subsequent lessons.

## Next Steps

In the next lesson, we will set up an AWS S3 bucket for storing NFT metadata, which is a crucial step in the architecture we discussed. [Deploy S3 Bucket for NFT Metadata with AWS CDK](../08-deploy-s3-bucket-for-nft-metadata-with-aws-cdk/README.md).
