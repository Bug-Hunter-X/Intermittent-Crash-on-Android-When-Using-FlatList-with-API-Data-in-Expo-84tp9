# Intermittent Crash on Android When Using FlatList with API Data in Expo

This repository demonstrates an uncommon bug encountered in an Expo React Native application.  The app fetches data from an API and displays it using a FlatList.  On Android devices, the app intermittently crashes without providing clear error messages in the logs.  The crash is not consistently reproducible, making debugging challenging.

## Bug Description

The app fetches character data from the Rick and Morty API.  The data is then rendered in a FlatList.  On certain Android devices, the app crashes randomly while scrolling through the list.  There are no specific triggers or patterns observed.

## Solution

The solution involves using `useMemo` to memoize the rendering of the list items. This prevents unnecessary re-renders that may contribute to the crashes.

## Reproduction Steps

1. Clone this repository.
2. Install dependencies: `npm install` or `yarn install`
3. Run the app on an Android emulator or device: `expo start`
4. Scroll through the list of characters. The app might crash intermittently.

## Additional Notes

This is a fairly uncommon error. The inconsistency makes pinpointing the root cause difficult without detailed debug logs or profiling tools.  The solution demonstrated here is a workaround that has shown improvement for this specific issue.
