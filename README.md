# gapi-client

A *very* thin Node wrapper for Google's client-side javascript V3 API.

## Example

```bash
npm install --save gapi-client
```

`index.js:`

```javascript
import gapi from 'gapi-client';

//On load, called to load the auth2 library and API client library.
gapi.load('client:auth2', initClient);

// Initialize the API client library
function initClient() {
  gapi.client.init({
    discoveryDocs: ["https://www.googleapis.com/discovery/v1/apis/drive/v3/rest"],
    clientId: 'YOUR_CLIENT_ID',
    scope: 'https://www.googleapis.com/auth/drive.metadata.readonly'
  }).then(function () {
    // do stuff with loaded APIs
    console.log('it worked');
  });
}

```

## License

MIT license.
