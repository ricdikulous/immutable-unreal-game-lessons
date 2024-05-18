# Retrieve Player Data with Immutable Passport

## Introduction
In this lesson, we will enhance our game by integrating player data retrieval utilizing the Immutable Passport. This functionality is key for personalizing the player experience, allowing us to display important player information such as wallet addresses and email addresses directly within the game.

## Lesson Objective
By the end of this lesson, you will be able to:
- Update the game instance to store player details such as wallet address and email.
- Enhance the login widget to retrieve these player details during the login process.
- Update the profile widget to display the retrieved player details.

## Overview
We will follow these steps to achieve our objective:
1. Update the game instance to store player details.
2. Enhance the login widget to retrieve player data.
3. Update the profile widget to display the retrieved data.
4. Test the changes and ensure the data is displayed correctly.

## Prerequisites
Before starting this lesson, make sure you have completed the previous lesson: [Log the Player in with the Immutable Passport](../04-log-the-player-in-with-the-immutable-passport/README.md). In the last lesson, we implemented player login functionality using Immutable Passport, enabling players to log in to the game securely.

## Step-by-Step Instructions

### Update the Game Instance
First, we need to update the game instance blueprint to store the player's email and IMX address.

1. Open the game instance blueprint.
2. Add two new variables:
   - `playerEmail` (String)
   - `playerIMXAddress` (String)
3. Save and compile the blueprint.

### Enhance the Login Widget to Retrieve Data
Next, we will enhance the login widget to retrieve the player's email and IMX address during the login process.

1. Open the login widget blueprint.
2. Delete the "Remove from Parent" node.
3. Add the "Is Registered Offchain" node.
   - Create a branch from its "Is Registered" pin.
   - Connect the branch to the "On Complete" pin of the "Is Registered Offchain" node.
4. If the player is not registered (false branch):
   - Add the "Register Off Chain" node.
   - From its "On Success" pin, add the "Get Address" node.
5. Connect the "Get Address" node to both branches (true and false) of the registration check.
6. From the "Got Address" pin, add the "Get Email" node.
7. Get the game instance and cast it to your specific game instance.
   - Connect this to the "Got Email" pin of the "Get Email" node.
8. Set the game instance variables:
   - Set `loggedIn` to true.
   - Set `playerIMXAddress` with the value from the "Get Address" node.
   - Set `playerEmail` with the value from the "Get Email" node.
9. Add back the "Remove from Parent" node to close the login widget and transition to the main menu.

### Update the Profile Widget
Now, we will update the profile widget to display the player's email and IMX address.

1. Open the profile widget blueprint.
2. On the "Construct" event:
   - Get the game instance and cast it to your specific game instance.
   - Set the text for `addressText` with the player's IMX address.
   - Set the text for `emailText` with the player's email.

### Testing Instructions
After making these changes, test the functionality:

1. Compile and run the game.
2. Log in and navigate to the profile page.
3. Verify that the player's email and IMX address are displayed correctly.
4. Ensure that the data retrieval works for both manual and saved credentials login flows.

## Conclusion
In this lesson, we enhanced our game by integrating player data retrieval using the Immutable Passport. We updated the game instance to store player details, enhanced the login widget to retrieve this data, and updated the profile widget to display it. This personalizes the player experience and ensures important information is readily accessible within the game.

## Next Steps
In the next lesson, we will implement player logout functionality. This will complete the login flow and ensure a seamless user experience. [Player Logout](../06-player-logout/README.md)
