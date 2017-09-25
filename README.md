# pwa-workshop
Simplyfied Progressive Web Application codelab based on:
https://codelabs.developers.google.com/codelabs/polymer-firebase-pwa
1. Create your project folder YOUR_PROJECT_NAME_FOLDER
2. `cd YOUR_PROJECT_NAME_FOLDER`
3. `npm install -g bower`
4. `npm install -g firebase-tools`
5. `firebase --version` (check firebase succesfull instalation, version must be 3+)
6. Open https://console.firebase.google.com/project and create new project
7. `firebase init`
  * Choose database and hosting
  * Choose default option (database.rules.json)
  * Choose default option (public)
  * Choose No for single page app
8. `cd public/`
9. `bower install -p polymerlabs/note-app-elements firebase/polymerfire PolymerElements/platinum-sw`
10. Create empty project files
  * touch manifest.json
  * touch public/sw-import.js
  * touch public/note-app.html
11. `firebase serve`
