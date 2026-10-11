# Buck's Spices for Claude

Meet the Spice Barista from [Buck's Spices](https://bucksspices.com), a family-run shop since 1973. Ask about small-batch spices, teas, culinary dried mushrooms, botanicals and hard-to-find ingredients. Get substitution ideas, links to the store's guides, and a prefilled cart for any recipe, after you confirm sizes and quantities.

The plugin uses public, read-only catalog tools without requiring a store login. It links directly to product pages and does not place orders or reserve inventory.

## Try these prompts

- What can I use instead of asafoetida?
- Build me a cart for nam ngiao.
- Gift ideas under $40 for a tea lover.
- What is dok ngiao, and how is it used in cooking?
- Tell me about your sencha and link a preparation guide.

## Data and privacy

Claude connects to Buck's public MCP endpoint at **https://answers.bucksspices.com/mcp**. When Claude calls a tool, it sends the following information to Buck's:

| Tool | Information sent |
| --- | --- |
| `search_products` | Your search query, optional category, stock-only preference and result limit. |
| `get_product` | A product ID or product handle. |
| `find_substitutes` | The ingredient name and any optional cooking context Claude includes. |
| `build_cart_link` | Selected variant IDs and quantities. |
| `search_guides` | Your guide search query and result limit. |

MCP initialization also sends client identification and protocol information. The plugin does not require your name, email, delivery address, payment information or full conversation. Avoid including personal details in queries or cooking context. Guide searches forward the search query to the Buck's Shopify storefront; catalog reads retrieve product data from Shopify, and guide results may also include public Spice Barista Corner Q&As. These tools do not call the Barista's language model.

Application tool logs record the tool name, latency, result count and an error flag. Tool arguments and conversation text are not logged by the MCP endpoint. The server uses the connecting IP address only for temporary, in-memory rate-limit counters; it does not write that IP address to its MCP application logs. Hosting providers may process network metadata separately.

Product prices and availability can be up to 15 minutes old; the server refreshes the catalog on demand and reports an error if fresh data cannot be loaded. Cart links open bucksspices.com, where the store's normal checkout and privacy practices apply.

## License

This plugin is distributed under the [MIT License](LICENSE).
