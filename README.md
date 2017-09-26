# pwa-workshop
Simplified Progressive Web Application codelab based on:
https://codelabs.developers.google.com/codelabs/polymer-firebase-pwa
1. Create your project folder YOUR_PROJECT_NAME_FOLDER
2. `cd YOUR_PROJECT_NAME_FOLDER`
3. `npm install -g bower`
4. `npm install -g firebase-tools`
5. `firebase --version` (check firebase succesfull instalation, version must be 3+)
6. Open https://console.firebase.google.com/project and create new project
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
`  <firebase-app`

        `name=""`

        `api-key=""`
        
        `auth-domain=""`
        `database-url=""`
        `project-id=""`
        `storage-bucket=""`
        `messaging-sender-id="">`
   `</firebase-app>`

13. `firebase serve`
14. Enable authentication in firebase console
15. Specify your project name in all components in `note-app.html`
    `app-name="YOUR_PROJECT_NAME"`
