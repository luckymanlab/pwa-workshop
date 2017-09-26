# pwa-workshop
Simplified Progressive Web Application codelab based on:
https://codelabs.developers.google.com/codelabs/polymer-firebase-pwa
1. Create your project folder YOUR_PROJECT_NAME folder
2. `cd YOUR_PROJECT_NAME`
3. `npm install -g bower`
4. `npm install -g firebase-tools`
5. `firebase --version` (check firebase succesfull instalation, version must be 3+)
6. Open https://console.firebase.google.com/project and create new project with YOUR_PROJECT_NAME
7. `firebase init`
  * Choose database and hosting
  * Choose created in firebase console project
  * Choose default option (database.rules.json)
  * Choose default option (public)
  * Choose No for single page app
8. `cd public/`
9. `bower install -p polymerlabs/note-app-elements firebase/polymerfire PolymerElements/platinum-sw`
10. Create empty project files
  * `touch manifest.json`
     Copy content from this repo `public/manifest.json`
  * `touch sw-import.js`
     Add `importScripts('bower_components/platinum-sw/service-worker.js');`
  * `touch note-app.html`
     Copy content from this repo `public/note-app.html`
11. Replace index.html content by content from this repo `public/index.html`
12. Update firebase component by your applicaion config from firebase app
    `<firebase-app ...></firebase-app>`
    and `name="..."` by YOUR_PROJECT_NAME
13. Specify pu YOUR_PROJECT_NAME as `app-name="..."` for `firebase-auth` `firebase-document` and `firebase-query` components in note-app.html
    `<firebase-app ...></firebase-app>`

14. `firebase serve`
15. Enable authentication in firebase console
16. Specify your project name in all components in `note-app.html`
    `app-name="YOUR_PROJECT_NAME"`
17. `firebase deploy`
