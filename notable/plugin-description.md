The Notable plugin provides a set of operations for interacting with Python notebooks in a project-based environment. Here are the details of the namespace and type definitions:

1. `create_notebook`: This operation creates a new notebook. If no project ID is provided, the user's default project will be used. The fields for this operation are:
    - `project_id`: The ID of the project to create the notebook in. This is optional.
    - `notebook_name`: The name of the notebook to create. This is optional and must end with .ipynb file extension.

2. `create_cell`: This operation creates a new cell in a notebook. The fields for this operation are:
    - `file_id`: The ID of the file to create the cell in. This is required.
    - `cell_type`: The type of cell to create. This can be "code", "markdown", or "sql".
    - `source`: Lines of source code to place in the cell. This is optional.
    - `sql_cell_handle`: The ID of the data source to use for a SQL cell. This is optional.
    - `after_cell_id`: The ID of the cell to insert this one after. If null, it'll be added to the end of the notebook. This is optional.

3. `get_cell`: This operation retrieves a cell from a notebook by its ID. The fields for this operation are:
    - `file_id`: The ID of the file to get the cell from. This is required.
    - `cell_id`: The ID of the cell to get. This is required.

4. `replace_cell_contents`: This operation replaces the source code of a cell. The fields for this operation are:
    - `file_id`: The ID of the file to replace the cell contents in. This is required.
    - `cell_id`: The ID of the cell to replace the contents of. This is required.
    - `source`: Lines of source code to replace the cell with. This is optional.

5. `run_cell`: This operation runs a cell within a notebook by its ID. The fields for this operation are:
    - `file_id`: The ID of the file to run the cell in. This is required.
    - `cell_id`: The ID of the cell to run. This is required.

6. `get_default_project`: This operation retrieves the user's configured default project. It does not require any fields.

7. `set_default_project`: This operation configures the user's default project (by UUID) for new notebooks. The fields for this operation are:
    - `new_default_project_id`: The new default project ID. This is required.

These operations allow for the creation, modification, and execution of cells within Python notebooks, as well as the management of projects within the Notable environment.
