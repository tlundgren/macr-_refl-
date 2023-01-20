# Macr- Refl-
A certain app for cloning disks and performing backups is distributed in different flavours that match paying and non paying users. Flavours differ in terms of features available. When a feature only available in a paying flavour of the app is selected by a non paying user, the programm reports the feature as being exclusive for paying users. The app can be upgraded to make all features available if a valid serial number is provided.

## Objectives
1-Have all features available to a non paying user.

## Work
1-The program reports its license type to the user when the About button is clicked. The logic here looks at two uninitialized global variables. It is enough to change the (only) routine that looks at one of these variables (which reports true if its value corresponds to a paying user, false otherwise) to have the whole app believe the user is paying a subscription and thus to make all features available.
Still, the program makes a license check on startup which finds the current serial number/license invalid (it is valid for a non paying version of the app) and so it reports. Still, the message can be closed and the app behaves normally.

2-Create an outbound firewall rule (Windows) to prevent any of the app's binaries from communicating with the outside - this prevents updates that would override the patch.

## What is Available
Nothing more than this document.

## License
This project is provided **AS-IS**.

This project is MIT licensed.
