# 06. Player Logout

## Introduction

Welcome back to our course on integrating NFTs into your Unreal Engine game using Immutable's SDK. In this lesson, we'll focus on implementing a secure logout functionality. Proper logout processes are crucial for games handling sensitive data, such as blockchain wallets and NFTs, to ensure that players can securely and efficiently end their sessions.

## Lesson Objective

By the end of this lesson, you will be able to:
- Implement logout functionality using Immutable Passport in Unreal Engine.
- Ensure players can securely log out, safeguarding their account and game data.

## Overview

In this lesson, we will cover the following steps:
1. Demonstrate the current state of the game without proper logout functionality.
2. Implement the logout feature using Unreal Engine blueprints.
3. Test and demonstrate the successful logout process.

## Prerequisites

Before starting this lesson, ensure you have completed the previous lesson on retrieving player data with Immutable Passport. [**Retrieve Player Data with Immutable Passport**](../05-retrieve-player-data-with-immutable-passport/README.md).

## Step-by-Step Instructions

### Demonstrating the Current State

Currently, our game automatically logs in with saved credentials and takes the player directly to the main menu. However, clicking the logout button does nothing. We'll address this by implementing proper logout functionality.

### Implementing Logout Functionality

1. **Open the Main Menu Widget**:
   - Navigate to the Main Menu Widget in your Unreal Engine project.
   - Locate the logout button's click event handler.

2. **Update the Logout Button Click Event**:
   - **Hide the Logout Button**: Set the visibility of the logout button to hidden to indicate that the logout process is starting.
   - **Show the Loading Throbber**: Set the visibility of a loading throbber to visible to indicate ongoing processing.

3. **Initiate Logout with Immutable SDK**:
   - Use the Immutable Logout node to initiate the logout process.
   - Print "Logging out..." to the debug console to confirm the process has started.

4. **Handle Successful Logout**:
   - Get the game instance and cast it to your specific game instance type.
   - Set the 'logged-in' variable to false to track the player's logged-out state.
   - Create and display the login widget, sending players back to the login screen.
   - Reset the visibility of the logout button and the loading throbber.

5. **Handle Logout Failure**:
   - Print "Logout failed" to the debug console.
   - Reset the visibility of the logout button and the loading throbber to allow the player to attempt logout again.

### Blueprint Overview

**Placeholder for Blueprint Example**

- **Logout Button Click Event**:
  - Set Visibility of Logout Button to Hidden
  - Set Visibility of Loading Throbber to Visible
  - Call Immutable Logout Node
  - Print "Logging out..." to Debug Console
  - On Success:
    - Get Game Instance
    - Set 'Logged-in' Variable to False
    - Create and Display Login Widget
    - Reset Visibility of Logout Button and Loading Throbber
  - On Failure:
    - Print "Logout failed"
    - Reset Visibility of Logout Button and Loading Throbber

### Demonstrating the Logout Process

1. Save and compile your blueprint changes.
2. Run the game and observe the automatic login with saved credentials.
3. Click the logout button to initiate the process.
4. Complete the logout process as prompted by the browser.
5. Observe the return to the login screen, confirming successful logout.
6. Restart the game to verify that it no longer logs in automatically with saved credentials.
7. Log in again to ensure the login functionality remains intact.

## Testing Instructions

To test the implementation:
1. Run the game and log in using saved credentials.
2. Click the logout button and follow the prompts to complete the logout process.
3. Verify that you are returned to the login screen.
4. Restart the game and confirm that it does not log in automatically.
5. Log in again and check that the main menu is accessible.

## Conclusion

In this lesson, we've successfully implemented a secure logout process using the Immutable SDK in our Unreal Engine game. This feature enhances the security and user experience by allowing players to securely end their sessions. 

## Next Steps

In the next lesson, we'll delve into the architecture of minting NFTs, exploring the necessary setup and integration for creating and managing NFTs within our game. Stay tuned! [**Overview of Minting Architecture**](../07-overview-of-minting-architecture/README.md)
