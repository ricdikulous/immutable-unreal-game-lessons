# Lesson 14: NFTs as Playable Characters

## Introduction
In this lesson, we will integrate NFTs as selectable, playable characters within our game. Currently, there's a disconnect between the NFTs in a player's inventory and the characters they can select for gameplay. Our goal is to bridge this gap, ensuring that the NFTs owned by a player are represented as characters in the game.

## Lesson Objective
By the end of this lesson, you will be able to:
- Integrate NFTs as selectable, playable characters within the game.
- Ensure that the character selection screen reflects the NFTs owned by the player.

## Overview
In this lesson, we will:
1. Review the current state of character selection in the game.
2. Understand the architecture for character representation.
3. Load NFTs from the server.
4. Update the character selection logic to include NFTs as playable characters.

## Prerequisites
Before you begin, ensure you have completed [Lesson 13: Display the NFTs in Game](../13-display-the-nfts-in-game/README.md). In this lesson, we set up the NFT inventory screen to display the NFTs owned by the player.

## Step-by-Step Instructions

### 1. Review Current State
Currently, the game shows only default characters in the character selection screen, even if the player owns NFTs. We need to fix this so that the character selection screen reflects the NFTs owned by the player.

### 2. Understand Character Architecture
- **Blueprints**: Characters in the game are represented as blueprints. Each blueprint includes the character's animation, skeleton, and properties like turning rate, top speed, acceleration, and the character name.
- **Data Table**: A data table stores the unique values for each character's traits, such as initial speed, top speed, and acceleration. The character name is used to look up the corresponding traits from the data table.

**Example Blueprint and Data Table:**
![Blueprint and Data Table Example](placeholder_for_blueprint_and_data_table_image)

- **Struct**: The struct represents the structure of our data in the data table.

**Example Struct:**
![Struct Example](placeholder_for_struct_image)

### 3. Load NFTs from Server
In the "Character Select Container" widget, we will:
1. Add an HTTP request to fetch the player's NFTs from the server.
2. Parse the JSON response into our NFT struct.

**Code Placeholder for HTTP Request:**
```plaintext
// Code to create and send HTTP request
// Parse JSON response into NFT struct
```

4. Update Character Selection Logic

    Modify the "Character Select Container" widget to check if the player owns an NFT for each character.
    If the player owns the NFT, add the character to the selection screen.

Blueprint Example for Character Selection Logic

// Blueprint logic to iterate through NFTs and add characters to the selection screen

## Testing Instructions

After implementing the above changes, run the game and navigate to the character selection screen. Ensure that the screen displays both the default characters and the NFTs owned by the player. When selecting a character, the correct character model should appear, and the character should be playable in the game.

## Conclusion

In this lesson, we integrated NFTs as selectable, playable characters within the game. We reviewed the current state of character selection, understood the architecture for character representation, loaded NFTs from the server, and updated the character selection logic.

## Next Steps

In the next lesson, we will explore how to mint NFTs in-game after collecting enough coins. Stay tuned!

Next Lesson: [Mint NFTs In-Game](../15-mint-nfts-in-game/README.md)