# rapp-sendemail
Send Email RApp (Robotic Application) for the RAPP Project

### User Credentials

Current implementation does not automatically retrieve user's email
credentials (username, password), as the RAPP Platform does not
provide such information at the moment!

User's email credentials can be passed to the application in the following ways:
- Append username and password credentials in a file under the same directory
of the application executable. That file should have the following format:

```
username: xxx
password: xxx
```

- Pass username and password credentials from command line, using the option
parser.

```bash
./app.py -u <username> -p <password>
```


### On-demand set destination email addresses

By default, the application user the **user_personal_info** RAPP Platform
Service to retrieve possible destination email addresses.

The application also accepts setting/appending destination email addresses
from command-line, using the `-d` option. Multiple email addresses can be passed,
separated by comma ",".

```bash
./app.py -d dest1@gmail.com,dest2@gmail.com
```
