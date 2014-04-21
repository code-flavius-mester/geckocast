# GeckoCast

Stream a GeckoBoard public URL to a Chromecast.

## Instructions

1. Go to https://cast.google.com/publish/#/signup and register as a Chromecast developer
2. Go to https://cast.google.com/publish/#/applications/new?type=web and setup a new Custom Receiver Chromecast app
    1. The URL should point to the receiver.html file that you've uploaded to your server
    2. Check Chrome box under Platforms
3. If you're not publishing to an SSL secured domain, you'll need to register a new Chromecast device as well
4. In index.html, set `data-application-id` on `<body>` to the application ID from the Google Cast SDK Console
5. In receiver.html, set the `src` of the `<iframe>` to the public URL of the dashboard you want to display
6. Browse to the index.html file in Chrome, then click the Chromecast extension button, then "Cast this Tab"

The dashboard will keep running if even you close the original tab or quit Chrome. You should only need to start casting again if the Chromecast goes offline.