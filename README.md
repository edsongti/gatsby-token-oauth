# gatsby-token-oauth

gatsby-token-oauth is a library for dealing with token.

## Installation

Use the npm to install gatsby-token-oauth.

```bash
npm install gatsby-token-oauth
```

## Usage

Create a .env file in the root of your project and inform the value of these variables:

```
GATSBY_SOURCE_ROOT=https://xxxxxxx
GATSBY_CLIENT_ID=xxxxx
GATSBY_CLIENT_SECRET=xxxxx
GATSBY_CLIENT_SCOPE=xxxxx
GATSBY_SOURCE_USER=xxxxx
GATSBY_SOURCE_PASSWORD=xxxxx
```

In your application, require and configure dotenv:

```es6
require("dotenv").config();
```

In your component:

```es6
import getToken from "gatsby-token-oauth";
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
