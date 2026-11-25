# SoChain MCP server

[![SoChain MCP connector](https://glama.ai/mcp/connectors/com.sochain/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.sochain/mcp)

SoChain's hosted MCP server gives AI agents Bitcoin, Litecoin, Dogecoin and Zcash blockchain data: address balances and transactions, unspent outputs, transactions, blocks and fee quotes. Testnets: BTCTEST (Bitcoin testnet4), LTCTEST, DOGETEST, ZECTEST.

- Endpoint: `https://sochain.com/mcp` (Streamable HTTP)
- No install: nothing runs on your machine.
- Works without a key, up to 2,500 lookups a day per IP.
- Optional API key, sent as the `API-KEY` header. A free account (email sign-in, no card) gets 75,000 requests a month; paid plans go higher. Get a key at https://sochain.com/dashboard. Plans: https://sochain.com/pricing.
- Read-only. It does not broadcast transactions.

Setup for other clients: https://sochain.com/agents. REST API docs: https://sochain.com/docs.

## Cline

Add this to `cline_mcp_settings.json` (MCP Servers > Configure):

```json
{
  "mcpServers": {
    "sochain": {
      "type": "streamableHttp",
      "url": "https://sochain.com/mcp",
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

With an API key, add a `headers` object:

```json
"headers": { "API-KEY": "your-sochain-api-key" }
```

## Tools

`search`, `get_balance`, `get_address_summary`, `get_transactions`, `get_transaction_counts`, `get_unspent_outputs`, `get_balance_history`, `get_address_rank`, `get_address_poisoning`, `get_counterparties`, `is_valid_address`, `get_transaction`, `get_transaction_status`, `get_block`, `get_latest_blocks`, `get_best_block_hash`, `get_network_info`, `get_price`, `get_chart`, `get_rich_list`.

## Support

support@sochain.com
