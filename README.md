# Akoya MCP Server

## How to Build

1. Install Node.js version 22 or greater. Check version with `node --version`.
2. Run `cd sdk && npm install` to go to the SDK folder and build the SDK.
3. Now run `cd ../mcp-server && npm install` to go to the server folder and build the server.

## How to Run

If you are not familiar with how to setup MCP Servers with Claude Desktop, see [this tutorial](https://modelcontextprotocol.io/quickstart/user) first.

Now add something like this to your Claude Desktop config:

```json
{
  "mcpServers": {
    "Akoya": {
      "command": "node",
      "args": ["[YOUR-PATH-HERE]/akoya-mcp-server-main/mcp-server/dist/index.js"],
      "env": {
        "AKOYA_AP_IS_V_2_4_0_LIB_ACCESS_TOKEN": "[YOUR-ACCESS-TOKEN-HERE]"
      }
    }
  }
}
```

A `claude_desktop_config.json` file is also provided as reference.

Make sure to set the path to the location where your MCP Server is stored as well as the access token you got after authenticating.

## How to Get Access Token

Follow [this guide](https://docs.akoya.com/docs/getting-started) to see how to get the access token to the Mikomo bank sandbox for Akoya.

## Usage Tips

- See [here](https://docs.akoya.com/docs/mikomo#mikomo-catalog) for a list of sandbox accounts. For best results, try [this personal finance account](https://docs.akoya.com/docs/pfm-test-user) or this [lending and credit account](https://docs.akoya.com/docs/lending-and-credit-test-user).
- Make sure to specify the date range you want when you are using the MCP Server in chat. The available date ranges are given for each account in the Akoya docs linked above.
- Username and password are always the same, for example the lending account has Username: `GenericUser_LendingAndCredit` and Password `GenericUser_LendingAndCredit`.