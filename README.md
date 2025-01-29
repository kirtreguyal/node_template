[develop-with-order](https://github.com/Skuukzkyy/node_template/tree/develop-with-order)

[develop-alert-checkout](https://github.com/Skuukzkyy/node_template/tree/develop-alert-checkout)

[develop-single-page-alert](https://github.com/Skuukzkyy/node_template/tree/develop-single-page-alert)


# Template Setup Guide

## Apps Needed

- Git
- VSCode
- MySQL
- Node.js

## Steps to Run the Template

1. **Clone the Repository**
    - Run the following command to clone the repository:
      ```bash
      git clone https://github.com/Skuukzkyy/node_template.git
      ```
    1.1 Open the cloned directory in VSCode.

2. **Install Dependencies**
    - Run the following command in the terminal to install the necessary dependencies:
      ```bash
      npm install
      ```

3. **Set Up the Database**
    - Open MySQL Workbench and create a new schema (database).

4. **Run Migrations**
    - Navigate to the `./migrations` folder and run the following files:
    
    4.1 **Create Tables**
    - Run the `create_tables.sql` file to create the necessary tables in your database.
      - Open it in MySQL Workbench and make sure to select the newly created schema as the default database before running the script.

    4.2 **Generate MySQL Queries**
    - Open the terminal and navigate to the `migrations` directory:
      ```bash
      cd migrations
      ```
    - Run the `generate_mysql_queries.sh` script:
      ```bash
      .\generate_mysql_queries.sh
      ```

    4.3 **Insert Data**
    - After running the `generate_mysql_queries.sh` script, a new file called `insert_queries.sql` should be created.
    - Open `insert_queries.sql` in MySQL Workbench and run it to insert the required product data.
      - Again, make sure to select the newly created schema as the default database before executing the script.

5. **Create `.env` File**
    - Create a new file called `.env` in the root directory of the project.
    - Use the following sample values to configure your environment variables:

    ```dotenv
    PORT=8080
    DATABASE_HOST=localhost
    DATABASE_USER=root
    DATABASE_PASSWORD=password
    DATABASE_NAME=tesda
    DATABASE_PORT=3306
    SESSION_SECRET=SECRET
    ```

6. **Run the Application**
    - Finally, run the development server by executing:
      ```bash
      npm run dev
      ```

Now, your application should be up and running!
