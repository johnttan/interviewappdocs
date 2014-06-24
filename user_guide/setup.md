# Setup

The setup process proceeds in 3 stages. Installation, Configuration, and Initialization.

- - -

###Installation

Using SQL server 2012 and IIS 8.0

1. Install **Node.js**
2. Install **IISnode**
3. Install **URL Rewrite module 2.0 for IIS**

###Configuration

1. Open **/lib/controllers/sqlconfig.js**
2. Enter appropriate values into the JSON.
    Example:

        exports.config = {

            user: 'TESTUSER',
            password: 'TESTPASSWORD',
            server: '127.0.0.1\\SQLEXPRESS',
            database: 'interviewapp'

        };
3. Set appropriate IIS settings. Port, domain, etc.
4. (If starting natively with node server.js command)

    Set environment variable **NODE_ENV** to 'production' and **PORT** to desired port.



###Initialization

1. Start site from the root app directory in IIS.
2. Go to **/setupsql**
3. The Questions table should be initialized in the database.
4. Go to **/setupkeys**
5. The Keys table should be initialized.
6. Go to **/setuprecent**
7. The Recent table should be initialized.
8. Double-check the SQL server for the correct tables being present.
9. The app is ready to use.


**Tips**

Make sure that the IIS site and App Pool has appropriate permissions to traverse the root site directory containing the site files. That is, the directory that contains the web.config file.
