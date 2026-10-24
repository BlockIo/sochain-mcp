# Installing the SoChain MCP server

SoChain is a hosted (remote) MCP server. There is nothing to clone, build or run.

1. Add this entry to the `mcpServers` object in `cline_mcp_settings.json`:

   ```json
   "sochain": {
     "type": "streamableHttp",
     "url": "https://sochain.com/mcp",
     "disabled": false,
     "autoApprove": []
   }
   ```

2. No API key is needed; it works keyless up to 2,500 lookups a day per IP. If the user has a SoChain API key (from https://sochain.com/dashboard), add `"headers": { "API-KEY": "<their key>" }` to the entry. Don't ask for a key unless the user wants higher limits.

3. Check it works: call `get_best_block_hash` with `network` set to `BTC`; it returns the latest block hash.

Networks: `BTC`, `LTC`, `DOGE`, `ZEC`, and testnets `BTCTEST` (Bitcoin testnet4), `LTCTEST`, `DOGETEST`, `ZECTEST`.
