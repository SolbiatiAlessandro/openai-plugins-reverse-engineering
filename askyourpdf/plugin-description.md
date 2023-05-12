The askyourpdf plugin is designed for downloading and searching through PDF documents to find answers to questions and retrieve relevant information. It interacts with a vector database to store and query the documents. The plugin has two main type definitions:

download_pdf_api_download_pdf_post: This type is used to download a PDF file from a URL and save it to the vector database. It requires a single field:

url: This is a string that represents the URL of the PDF document to be downloaded.
perform_query_query_post: This type is used to perform a query on a document that has been previously downloaded and saved to the vector database. It requires two fields:

doc_id: This is a string that represents the identifier of the document in the database.
query: This is a string that represents the question or query to be asked based on the PDF document.
The plugin is used whenever a user asks something that might be found in a PDF document. The assistant is also expected to include the page number where the answer was found.
