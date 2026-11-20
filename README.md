# HenryCrawl E-commerce MCP: Amazon, eBay, 1688

Amazon, eBay and 1688/AliExpress product data for AI agents: prices, demand, sold counts, factory costs.

**For:** Online sellers, dropshippers, pricing analysts and sourcing agents.
**4 tools**, pay per result (no subscription), callable from Claude, ChatGPT, Cursor or any MCP client.

| Tool | Price |
|---|---|
| [Amazon Product Scraper - Prices, ASIN & Demand Signal](https://apify.com/henrycrawl/amazon-products-scraper) | $0.005 per row ($5 per 1,000) |
| [eBay Scraper - Listings, Sellers & Sold Price Check](https://apify.com/henrycrawl/ebay-listings-scraper) | $0.0035 per row ($3.50 per 1,000) |
| [eBay Seller Scraper - Full Store Inventory & Price Stats](https://apify.com/henrycrawl/ebay-seller-scraper) | $0.004 per row ($4 per 1,000) |
| [China Sourcing Finder: 1688 Factory vs AliExpress Prices](https://apify.com/henrycrawl/china-sourcing-finder) | $0.004 per product found ($4 per 1,000). Error rows and blocked pages are not charged. |


## Remote MCP server for the whole bundle
Remote URL (Claude "Add custom connector", Cursor, any MCP client):

```
https://mcp.apify.com/?tools=henrycrawl/amazon-products-scraper,henrycrawl/ebay-listings-scraper,henrycrawl/ebay-seller-scraper,henrycrawl/china-sourcing-finder
```

Claude Desktop (`claude_desktop_config.json`), using your own Apify token: each call is billed to your Apify account at the prices above.

```json
{
  "mcpServers": {
    "henrycrawl-thuong-mai-dien-tu": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://mcp.apify.com/?tools=henrycrawl/amazon-products-scraper,henrycrawl/ebay-listings-scraper,henrycrawl/ebay-seller-scraper,henrycrawl/china-sourcing-finder",
        "--header",
        "Authorization:Bearer ${APIFY_TOKEN}"
      ],
      "env": {
        "APIFY_TOKEN": "<your Apify API token>"
      }
    }
  }
}
```


## Key features
- Amazon search with 'bought in past month' demand signal
- eBay sold counts and full competitor-store inventory
- 1688 factory price vs AliExpress retail price side by side
- Pay per result, error rows and blocked pages not charged on sourcing

## Example uses
- Ask Claude: 'find 3 products under $20 on Amazon with high monthly sales and compare 1688 factory cost'
- Monitor a competitor's eBay store prices and conditions weekly

## FAQ
**How am I billed?**
Each call runs an Apify actor on your own Apify account, billed per product returned ($3.50 to $5 per 1,000). No subscription.

**Which marketplaces are covered?**
Amazon search results, eBay listings and seller stores, 1688.com and AliExpress.

**Is there free usage?** New Apify accounts get monthly free platform credit, enough to try every tool.

---
Built and maintained by **HenryCrawl** ([Apify Store](https://apify.com/henrycrawl)). Issues and feature requests: open a GitHub issue here.
