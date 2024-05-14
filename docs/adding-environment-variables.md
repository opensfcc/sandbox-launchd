![Logo](https://avatars.githubusercontent.com/u/151680118?s=200&v=4 "Logo")

**[↤ Getting Started](../README.md)**

Adding Environment Variables
===

> We'll need the following Environmental Variables to be set before things will work.

Add the following under the existing exports listed in your `~/.zshrc`

```bash
# SFCC-CI Variables
export SFCC_OAUTH_CLIENT_ID="1a2b3c4d-5e6f-7g8h-9i0j-1k2l3m4n5o6p"
export SFCC_OAUTH_CLIENT_SECRET="my^super*secret+password"
export SFCC_SANDBOX_ID=""
```

### What do these do?

* `SFCC_OAUTH_CLIENT_ID` - This is your "API Client" that was generated earlier
* `SFCC_OAUTH_CLIENT_SECRET` - This is the password you entered earlier
* `SFCC_SANDBOX_ID` - We'll be getting this in a few steps

Now we need to reload our profile:

```bash
source ~/.zshrc
```

---

[![Previous Step](https://img.shields.io/badge/Previous-121212.svg?logo=github&style=for-the-badge)](./create-api-client.md) &nbsp; [![Next Step](https://img.shields.io/badge/Next_Step-1aa0db.svg?logo=github&style=for-the-badge)](./test-sfcc-ci.md)
