# Install the Immutable SDK into Unreal Engine

## Lesson Introduction
Welcome to this lesson of our course on integrating the [Immutable SDK for Unreal Engine](https://github.com/immutable/unreal-immutable-sdk.git). Today, we're diving into the installation of the Immutable SDK, the first step in bringing blockchain functionalities into your game.

## Lesson Objective
By the end of this lesson, you will have successfully installed the Immutable SDK into your Unreal Engine project, preparing it for blockchain functionalities.

## Overview
In this video, we'll cover the following steps:
1. Cloning the Unreal Immutable SDK into your project.
2. Opening the project and letting it build the modules.
3. Verifying that the plugin is operational within Unreal Editor.

## Prerequisites
Before starting this lesson, ensure you have:
- Git installed on your system.
- Git Large File Storage (LFS) installed.

## Detailed Explanation

### Step 1: Install Git LFS
Since .uasset and .umap files are stored on Git Large File Storage, you must download and install Git LFS from the [official website](https://git-lfs.com/).

### Step 2: Clone the Unreal Immutable SDK
Navigate to the GitHub page for the [Unreal Immutable SDK](https://github.com/immutable/unreal-immutable-sdk.git). From here, you can either download the repository or clone it. 

To clone the repository, Navigate to your project's Plugins directory and clone the repo:

```
cd MyGame/Plugins
git clone https://github.com/immutable/unreal-immutable-sdk.git
```

If you chose to download the SDK, make sure to unzip it and move it to your project's Plugins directory.

### Step 3: Open the Project
Open the project in the Unreal Editor. If prompted to rebuild the modules, select 'Yes'. This will allow Unreal to integrate the new plugin.

### Step 4: Verify the Plugin
Once the editor is open and the modules have been successfully built, you should see the Immutable SDK in the Plugins folder. You can explore the Immutable Content folder and check out the Blueprint Sample content to see what blueprints using the Immutable SDK look like.

## Testing Instructions
- Open Unreal Engine and navigate to the Plugins folder.
- Verify that the Immutable SDK is listed and active.
- Explore the Immutable Content folder to see sample blueprints.

## Conclusion
In summary, we:
- Cloned the Unreal Immutable SDK into our Plugins folder.
- Opened the project and allowed it to build the new plugin.
- Confirmed that the plugin is loaded correctly within the Unreal Editor.

## Next Steps
In the next lesson, we'll register the game on the Immutable Hub and set up the necessary details to log our players in. See you in the next video!

[**Register the Game on the Immutable Hub**](../03-register-the-game-on-the-immutable-hub/README.md)
