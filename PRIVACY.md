# Buck's Spices MCP privacy notice

Effective October 18, 2026.

Buck's Spices, operated by Culex Inc., provides the public MCP service at https://answers.bucksspices.com/mcp. This notice explains how the service handles information when you use the Buck's Spices connector or Claude plugin. It supplements the [Buck's store privacy policy](https://bucksspices.com/policies/privacy-policy), which applies when you visit the store or use its checkout.

## Information the service receives

When Claude calls a tool, it sends the inputs needed for that tool:

| Tool | Inputs |
| --- | --- |
| `search_products` | Search query, optional category, stock preference and result limit. |
| `get_product` | Product ID or product handle. |
| `find_substitutes` | Ingredient name and optional cooking context. |
| `build_cart_link` | Selected product variant IDs and quantities. |
| `get_starter_kit` | Cuisine and optional region. |
| `find_published_recipe` | Dish name and optional chef or restaurant. |
| `search_guides` | Search query and result limit. |

The connection also supplies MCP client and protocol information, HTTP connection metadata and the connecting IP address. For a remote Claude connector, the connecting address may belong to Anthropic's infrastructure rather than your device.

The service does not require a Buck's account, name, email address, delivery address or payment information. It does not request your full conversation, Claude memory, chat history or uploaded files. If personal information is included in a query or cooking context, it reaches the service as part of that input. Please omit personal or sensitive information from tool inputs.

## How information is used

Tool inputs are used to answer the requested product, ingredient, recipe-source or guide query, or to validate a shopping link. Connection information supports delivery, security and rate limiting. The tools do not place orders, reserve inventory or modify store content.

The MCP tools do not call the Spice Barista's language model. Tool inputs are not used by this service to train an AI model or build customer profiles, and the service does not sell those inputs or share them for targeted advertising.

## Storage and retention

- **Tool inputs and responses:** The MCP application processes these in memory for the request and does not save their contents to its application logs, a customer database or a conversation history. Ending a request does not guarantee immediate erasure from process memory. Claude separately receives the response under its own data practices.
- **Rate-limit counters:** The application keeps the connecting IP address, a window start time and request count in memory. Windows last 60 seconds. Expired entries are removed when the next request is handled; all entries disappear when the process restarts. An idle process may retain an expired entry until one of those events.
- **Application operational logs:** The MCP application logs the tool name, elapsed time, result count and whether an error occurred. It does not include tool arguments, response bodies, conversation text or connecting IP addresses in those log entries. Railway captures these logs under its plan-dependent retention settings. Its [log-retention documentation](https://docs.railway.com/observability/logs#log-retention) describes viewing windows and notes that upgrading plans can restore older logs. A viewing window is not a guarantee of permanent deletion.
- **Provider metadata:** Hosting and upstream providers may retain connection, security and operational records under their own policies. Railway describes retention based on service provision, business purposes, legal obligations and dispute resolution in its [privacy policy](https://railway.com/legal/privacy). This notice does not promise a fixed deletion deadline for records controlled by those providers.
- **Support correspondence:** If you contact Buck's, the information you provide is retained as needed to answer your request, follow up on unresolved issues and meet applicable recordkeeping obligations.

The cached product catalog contains store product data, not a history of your tool queries.

## Service providers and disclosures

**Railway** hosts the service and processes requests and infrastructure metadata to deliver it. See [Railway's privacy policy](https://railway.com/legal/privacy).

**Shopify** supplies Buck's product catalog and storefront search. Product catalog reads retrieve store product data. Guide searches send the guide query to Buck's Shopify storefront; the service also searches already-public Spice Barista Corner Q&As. Shopify may process those requests under its [privacy policy](https://www.shopify.com/legal/privacy). MCP queries do not create customer accounts, marketing subscriptions or new public Q&As.

**Anthropic** operates Claude and delivers tool calls and results. Your conversations and connector use within Claude are governed by [Anthropic's privacy policy](https://www.anthropic.com/legal/privacy) and your account settings. This notice covers Buck's service, not Anthropic's storage of your chat.

Information may also be disclosed where required by applicable law or to address security incidents and protect legal rights. Providers may process information in countries other than your own.

## Store links and attribution

Returned Buck's product, guide and cart links include UTM parameters identifying Claude as the referral source and the tool that generated the link. Cart links contain selected variant IDs and quantities and may include a configured discount code. These parameters do not add your name, email address or conversation text.

Opening a link sends a normal web request to its destination. Store browsing, cookies, purchases and checkout are covered by the [store privacy policy](https://bucksspices.com/policies/privacy-policy); third-party recipe sites apply their own policies. Generating a shopping link does not itself complete a purchase.

## Your choices and contact

You can stop sending new requests by disabling or removing the connector in Claude. Removing it does not automatically delete records already held by Anthropic or other providers. For requests concerning those providers' records, use their privacy controls and contact channels.

For questions, security concerns or requests to access, correct or delete personal information held by Buck's in connection with this service, email [bucksspices@gmail.com](mailto:bucksspices@gmail.com). Available rights depend on applicable law; records may need to be retained where legally required. Because this service does not keep an account-linked query history, we may not be able to identify a past request from an email address alone. Please do not send passwords or payment information.

Material changes to this notice will be reflected in its effective date and the public repository history.
