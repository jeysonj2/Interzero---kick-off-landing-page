# Setup

1. Run `docker compose up -d`
2. Go to the browser and open http://localhost
3. Follow the steps to install Wordpress (Set any user and password, they will be replaced later)
4. Install the migration plugin, [All-in-One Migration](https://wordpress.org/plugins/all-in-one-wp-migration/)
5. Go to the backups folder and uncompress the zip file which contains the .wpress backup file
6. Import the backup (the .wpress file in the backups folder)
7. Login again, the default user and password are:
   - `info@decodeit.co`
   - `K1ck0ff_W0rdPr3ss!`

## Forcing a new password for the default user

1. Go to the browser and open https://www.miraclesalad.com/webtools/md5.php
2. Enter the desired password in the `String(s)` field
3. Copy result from the `MD5 Hash(es)` field
4. Open the database client of your preference (DBeaver, PHPAdmin). The access data should be as following, however, if they are not working please check the `.env` file:
   - User: `wp_kickoff`
   - Password: `K1ck0ff_W0rdPr3ss!`
   - Database: `wp_kickoff`
5. Open the wp_users table
6. Paste the hash that you copied in the step 3
7. Save the new data
8. Now you can login in Wordpress using the new password
