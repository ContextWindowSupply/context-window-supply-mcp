# Context Window Supply MCP server

Browse merch for AI builders, get US shipping quotes, and create Stripe checkout links.

Context Window Supply is a small online store of tees, hoodies and a sticker sheet for people who build with AI. This MCP server lets an AI agent search the catalog, read sizes, colors and prices, quote US shipping, and create a checkout link. A person opens that link and pays on Stripe. The agent never handles payment details.

Product images are digital previews.

## Endpoint

- URL: `https://contextwindowsupply.com/mcp`
- Transport: Streamable HTTP
- Auth: none
- MCP Registry name: `com.contextwindowsupply/store`

## Tools

| Tool | What it does |
|---|---|
| `search_products` | Search the catalog by keyword or product type (tee, hoodie, sticker). |
| `get_product` | Get one product's sizes, colors and price. |
| `get_shipping_quote` | Quote US shipping for a cart. |
| `create_checkout_link` | Create a Stripe checkout link a person opens to pay. |

## Connect

Add this to an MCP client config (Claude Desktop, Cursor and others that support remote servers):

```json
{
  "mcpServers": {
    "context-window-supply": {
      "url": "https://contextwindowsupply.com/mcp"
    }
  }
}
```

## Notes

- Ships to the US only. Prices include tax.
- This repo holds documentation only. It contains no store code and no keys.
- Store: https://contextwindowsupply.com
- Contact: hello@contextwindowsupply.com
