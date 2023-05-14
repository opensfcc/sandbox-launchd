![Logo](https://sfccdevops.s3.amazonaws.com/logo-128.png "Logo")

**[↤ Getting Started](../README.md)**

Fetch Sandbox UUID
===

> Now that we've verified everything is working with SFCC-CI, we can get our Sandbox UUID.

Let's get a list of sandboxes our API Client ID has permission to access:

```bash
sfcc-ci sandbox:list
```

Using the table generated in the command above, look for your sandbox number in the `instance` column.  For example, if your sandbox starts with `abcd-001` your `instance` will be `001`.

Copy the `id` from the `id` column for your sandbox.

Now we can paste our Sandbox UUID as the value for `SFCC_SANDBOX_ID` in our `~./zshrc` file.

```bash
export SFCC_SANDBOX_ID="9p8o7n6m-5l4k-3j2i-1h0g-9f8e7d6c5b4a"
```

Now let's reload our profile again with this update:

```bash
source .zshrc
```

---

[![Previous Step](https://img.shields.io/badge/Previous-121212.svg?logo=github&style=for-the-badge)](./test-sfcc-ci.md) &nbsp; [![Next Step](https://img.shields.io/badge/Next_Step-1aa0db.svg?logo=github&style=for-the-badge)](./install-launch-agents.md)
