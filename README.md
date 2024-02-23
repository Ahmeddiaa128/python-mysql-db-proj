# python-mysql-db-proj
Flask application that serves a RESTful API for managing a database table (example_table) and a basic user interface (UI) for interacting with it:

# HTML UI (index.html):
The UI consists of a form to insert records and a section to view existing data.
The form allows users to input a name and insert a record into the database table.
Existing data is displayed as a list (<ul> element) with each record's ID and name.
# Python Flask Application:
1. Imports:

Flask: The Flask web framework.
jsonify: A Flask helper function to jsonify Python objects.
render_template: A Flask function to render HTML templates.
request: A Flask object that represents the HTTP request.
pymysql: A Python MySQL client library.
2. Database Connection (get_db_connection):

Establishes a connection to a MySQL database hosted on Amazon RDS.
3. Routes:

/health: Returns a simple "Up & Running" message to check if the application is running.
/create_table: Creates the example_table if it doesn't exist in the database.
/insert_record: Handles POST requests to insert records into the example_table.
/data: Retrieves all records from the example_table and returns them as JSON.
/: Renders the index.html template for the UI.
4. Main Function:

Runs the Flask application with debug mode enabled, allowing for automatic reloading and showing detailed errors. The host is set to 0.0.0.0, meaning it will be accessible from any network interface.
