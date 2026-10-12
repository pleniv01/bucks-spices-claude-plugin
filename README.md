# Buck's Spices for Claude

Meet the Spice Barista from [Buck's Spices](https://bucksspices.com), a family-run shop since 1973. Ask about small-batch spices, teas, culinary dried mushrooms, botanicals and hard-to-find ingredients. Get substitution ideas, links to the store's guides, and a prefilled cart for any recipe, after you confirm sizes and quantities.

Ask how a favorite restaurant dish is made and get a home version with the spices to match. Find the essential spices of a cuisine, including the flavors of home. Cart links include 10% off for Claude users.

The plugin uses public, read-only catalog tools without requiring a store login. It links directly to product pages and does not place orders or reserve inventory.

## Try these prompts

- What can I use instead of asafoetida?
- What are Tasmanian peppercorns, and how do I cook with them?
- How can I make a copycat version of a famous fried chicken seasoning at home?
- My family is from Addis Ababa. What spices do I need to cook the food I grew up with?
- Build me a cart for chicken tikka masala.

## Data and privacy

Claude connects to Buck's public MCP endpoint at **https://answers.bucksspices.com/mcp**. When Claude calls a tool, it sends the following information to Buck's:

| Tool | Information sent |
| --- | --- |
| `search_products` | Your search query, optional category, stock-only preference and result limit. |
| `get_product` | A product ID or product handle. |
| `find_substitutes` | The ingredient name and any optional cooking context Claude includes. |
| `build_cart_link` | Selected variant IDs and quantities. |
| `get_starter_kit` | The cuisine and optional region. |
| `search_guides` | Your guide search query and result limit. |

MCP initialization also sends client identification and protocol information. The plugin does not require your name, email, delivery address, payment information or full conversation. Avoid including personal details in queries or cooking context. Guide searches forward the search query to the Buck's Shopify storefront; catalog reads retrieve product data from Shopify, and guide results may also include public Spice Barista Corner Q&As. These tools do not call the Barista's language model.

Application tool logs record the tool name, latency, result count and an error flag. Tool arguments and conversation text are not logged by the MCP endpoint. The server uses the connecting IP address only for temporary, in-memory rate-limit counters; it does not write that IP address to its MCP application logs. Hosting providers may process network metadata separately.

Product prices and availability can be up to 15 minutes old; the server refreshes the catalog on demand and reports an error if fresh data cannot be loaded. Cart links open bucksspices.com, where the store's normal checkout and privacy practices apply.

Links to bucksspices.com include standard tracking parameters (utm_source=claude) so Buck's can see visits and orders that came from Claude, and cart links may include the Claude discount code. They contain no personal information.

## License

This plugin is distributed under the [MIT License](LICENSE).
