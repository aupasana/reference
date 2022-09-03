# Storing secrets in OSX 

The `security` command can be used to store and retrieve secrets from your keychain.

### Store secrets in your keychain from the command-line

`security add-generic-password -s 'SECRET_NAME' -a 'USER_NAME' -w 'PASSWORD'`

This command stores secrets in keychain. You can also do this via the `Keychain Access` GUI application.

### Retrieve secrets from your keychain from the command-line

`security find-generic-password -gs "SECRET_NAME" -w | tr -d '\n'`

This command retrieves the password. It prints it to the command line with a training newline, which the `tr` command strips off.
There is no option to display only the account string (i.e. USER_NAME). 

To get USER_NAME, dump all the properties, and use sed to extract it

`security find-generic-password -gs "SECRET_NAME" 2>&1 | grep acct | sed 's:^ *"acct\"<blob>="\(.*\)"$:\1:' | tr -d '\n'`
