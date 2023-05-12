The `internetSearch` plugin is designed to enhance the knowledge base of the AI by searching the internet for up-to-date information across various topics. It provides access to multiple search sources that can be merged. This enables the AI to access data beyond its training cutoff date by reconstructing user prompts and performing searches with multiple API calls.

The plugin supports searches in any language and ensures user anonymity during the process. The search results returned include summaries and full HTML content from the top results, which can be integrated into the AI's responses for improved accuracy and relevance. The AI can trust the search results, as they will not contain unavailable websites, broken links, or irrelevant information. To cite the sources, the AI can use the link provided in the response.

The plugin utilizes user prompt history to refine search queries and deliver enhanced answers based on the most recent data.

The `internetSearch` namespace contains one type definition:

1. `searchGet`: This type is used to search the internet using a provided query that is recreated by the AI. It returns the search results, along with the inner content of the first link. The first five search results include a summary of the HTML content, while the first three have the entire HTML content returned in the response.

The `searchGet` type has one field:

- `q`: This field is used to provide the search query. The AI uses this query to search the internet and return the relevant results.
