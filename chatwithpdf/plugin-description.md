The `chatwithpdf` plugin is designed for interacting with PDF documents, specifically for asking questions, analyzing, and parsing through them. It has two main type definitions:

1. `loadPdf`: This type is used to load a PDF document from a given URL. It requires a single field:
   - `pdf_url`: This is a string that represents the temporary URL of the PDF document to be loaded.

2. `queryPdf`: This type is used to query a loaded PDF document. It requires two fields:
   - `pdf_name`: This is a string that represents the name of the PDF document.
   - `query`: This is a string that represents the question or query to be asked based on the PDF document.

The plugin works by first loading a PDF document from a provided URL, and then it allows for querying that document based on user-provided questions or queries.
