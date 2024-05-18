# Register the Game on the Immutable Hub

## Lesson Objective
Guide students through the process of setting up a project on Immutable Hub and configuring the Unreal Engine game instance.

## Overview
In this lesson, you will:
- Set up a new project in Immutable Hub.
- Configure client settings in Immutable Hub.
- Update the game instance in Unreal Engine with the necessary values from Immutable Hub.

## Prerequisites
Before starting this lesson, make sure you have completed the following:
- [**Course Introduction**](../01-course-introduction/README.md)
- [**Install the Immutable SDK into Unreal Engine**](../02-install-the-immutable-sdk-into-unreal-engine/README.md)

## Step-by-Step Instructions

### Step 1: Set Up the Project in Immutable Hub
1. Navigate to the [Immutable Hub website](https://hub.immutable.com/) and log in or create a new account.
2. Click on **Add Project**.
3. Name your project **Unreal Run Game**.
4. Select **Immutable ZKEVM** as the environment.
5. Create an environment named **test** using the testnet settings. This allows you to test without using real transactions.

### Step 2: Configure Client in Immutable Hub
1. Navigate to the **Passport** tab in your project.
2. Create a default client.
3. Configure the redirect URL as `rungame://callback` and the logout URL as `rungame://logout`.
4. Save these changes.
5. Note down the **Client ID**, **Redirect URI**, and **Logout URI**.

### Step 3: Configure Game Instance in Unreal Engine
1. Open your Unreal Engine project.
2. Navigate to your custom **Game Instance** blueprint, named `run-game-instance`.
3. Create variables for:
    - Client ID
    - Redirect URI
    - Logout URI
    - Environment
4. Compile the blueprint to add default values:
    - Set the **Client ID** with the value from Immutable Hub.
    - Set the **Redirect URI** with `rungame://callback`.
    - Set the **Logout URI** with `rungame://logout`.
    - Set the **Environment** to `"sandbox"`.

### Step 4: Code Implementation in the Game Instance
- **Placeholder for Blueprint Example**
- Add nodes to initialize the Immutable Passport using the stored Client ID and Redirect URI, adjusting for platform specifics.

## Testing Instructions
1. Ensure all variables in the Game Instance are set correctly.
2. Test the game to verify that the Immutable Passport initializes correctly using the provided credentials.

## Conclusion
In this lesson, we set up a project on Immutable Hub and configured our Unreal Engine game instance with the necessary credentials. This setup is crucial for logging players into the game using the Immutable Passport.

## Next Steps
In the next lesson, we will log our players in using the Immutable Passport.

[**Log the Player in with the Immutable Passport**](./lessons/04-log-the-player-in-with-the-immutable-passport/README.md)
