# Register the Game on the Immutable Hub

## Lesson Introduction
In this lesson, we will register our game on the [Immutable Hub](https://hub.immutable.com/). This is a necessary step to utilize the Immutable SDK for player authentication in our Unreal Engine game. By the end of this lesson, you will have set up your project on the Immutable Hub and configured your Unreal Engine game instance with the necessary credentials.

## Lesson Objective
By the end of this lesson, you will be able to:
- Register a game project on the [Immutable Hub](https://hub.immutable.com/).
- Set up the Immutable Passport with appropriate credentials.
- Configure the Unreal Engine game instance with the necessary variables for the Immutable SDK.

## Overview
In this lesson, we will:
1. Navigate to the [Immutable Hub](https://hub.immutable.com/) website and log in.
2. Create a new project on the Immutable Hub.
3. Set up the client configuration for the Immutable Passport.
4. Configure the game instance in Unreal Engine with the obtained credentials.

## Prerequisites
Before starting this lesson, ensure you have completed the previous lesson on [Installing the Immutable SDK into Unreal Engine](../02-install-the-immutable-sdk-into-unreal-engine/README.md). This provides the necessary setup for integrating Immutable's technology into your Unreal Engine project.

## Step-by-Step Instructions

### Step 1: Set Up the Project in Immutable Hub
1. **Navigate to the Immutable Hub**: Go to the [Immutable Hub](https://hub.immutable.com/) website and log in. If you don't have an account, create one.
2. **Create a New Project**: Follow the prompts and fill in the appropriate values for your game. We will set up an environment named "test" use the testnet settings.

### Step 2: Configure Client in Immutable Hub
**Create the Client**:
   - Navigate to the "Passport" tab and create the default client.
   - Select the "native" client for our game.
   - Generally, the default settings are okay if you don't need to support PKCE.
   - If you need to support PKCE, add the redirect URL: `rungame://callback` and the logout URL: `rungame://logout`.
   - Save the configuration and note the Client ID for later use.

### Step 3: Configure Game Instance in Unreal Engine
We are saving these values in our custom game instance so that we can access them later in our game when we need to authenticate the player and interact with the Immutable Passport.

1. **Open Unreal Engine**: Navigate to your Unreal Engine project.
2. **Configure the Game Instance**:
   - Open the `RunGameInstance` blueprint.
   - Add new variables for the following and set their default values:
     - **Client ID**: Obtain from the client above.
     - **Redirect URI**: `rungame://callback` (only if supporting PKCE).
     - **Logout URI**: `rungame://logout` (only if supporting PKCE).
     - **Environment**: Set to **sandbox** for testnet.

## Conclusion
In this lesson, you registered your game on the [Immutable Hub](https://hub.immutable.com/) and configured the game instance in Unreal Engine with the necessary credentials. This setup is crucial for authenticating players using the Immutable Passport.

## Next Steps
In the next lesson, we will focus on [Logging the Player in with the Immutable Passport](../04-log-the-player-in-with-the-immutable-passport/README.md). This will allow us to authenticate players within our game environment.