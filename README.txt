INANDA BUSINESS WEB - installable web app (PWA)

FILES (keep them together, exactly like this):
  index.html            the app
  manifest.webmanifest  name, colours and icons for installing
  sw.js                 makes it work offline and installable
  icons/                app icons

STEP 1 - PUT IT ONLINE (must be https)
  Upload this whole folder to any https host, for example:
  - Netlify: drag the folder onto app.netlify.com/drop
  - Cloudflare Pages, GitHub Pages or Firebase Hosting
  Test on your own computer first: open a terminal in this folder and run
      python3 -m http.server 8000
  then open http://localhost:8000 in Chrome. (Opening index.html by double-click will NOT install.)

STEP 2 - INSTALL
  Chrome on Android: an "Install app" card appears, or menu (three dots) > Install app.
  Chrome on computer: click the install icon at the right of the address bar.
  Safari on iPhone/iPad: tap Share > Add to Home Screen > Add.
  Safari on Mac: File > Add to Dock.

UPDATING LATER
  After you change any file, change VERSION in sw.js (e.g. "inanda-v2") before uploading.

IMPORTANT
  This is still the prototype: orders, bills and logins live only in the browser and reset when
  the page reloads. Real orders and payments need the database (takeaway-app-schema.sql) and a server.
