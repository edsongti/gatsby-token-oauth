# token-drupal-oauth2

token-drupal-oauth2 is a library for dealing with drupal token.

## Installation

Use the npm to install token-drupal-oauth2.

```bash
npm install token-drupal-oauth2
```

## Usage

Create a .env file in the root of your project and inform the value of these variables:

GATSBY_DRUPAL_ROOT=https://xxxxxxx
GATSBY_CLIENT_ID=xxxxx
GATSBY_CLIENT_SECRET=xxxxx
GATSBY_CLIENT_SCOPE=xxxxx
GATSBY_DRUPAL_USER=xxxxx
GATSBY_DRUPAL_PASSWORD=xxxxx

In your application, require and configure dotenv:

```es6
require("dotenv").config();
```

In your component:

```es6
import getToken from "token-drupal-oauth2";
```

And get a token:

```es6
const token_data = getToken();
```

getToken() will return a object json like this:

```json
access_token: "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1Ni",
expires_in: 300,
refresh_token: "def5020097271b1207d45e25b65a7a7db5",
token_type: "Bearer"
```

## Dependencies

- [dotenv](https://www.npmjs.com/package/dotenv)
- [axios](https://www.npmjs.com/package/axios)

## License

[MIT](https://choosealicense.com/licenses/mit/)
