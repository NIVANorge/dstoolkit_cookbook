# Configure `pylint`

[pylint](https://pypi.org/project/pylint/) is a static code analyser designed to help programmers write better code. It analyses code as you type (without actually running it) and checks for errors and formatting issues.

Although useful, pylint can sometimes be a bit "enthusiastic" - especially in a notebook environment where users are typically writing quick scripts rather than "production" code. 

**It is recommended to follow code style best practices where possible**, but if you're finding pylint's style warnings annoying rather than helpful, you can configure them as follows:

 1. Sign in to JupyterHub, open a new **terminal** and run
 
            pylint --generate-rcfile > ~/.pylintrc
            
 2. Start **VSCode** and open the new file named `.pylintrc`, which you will find in the top level of your `HOME` directory. (Note that the `.` at the start of the filename makes this a "hidden" file, so it does not appear in the JupyterLab file browser, but it is visible in VSCode).
 
 3. Scroll down to the `disable` section of the configuration file (line 411). You can either disable specific warnings or disable everything. For example:
 
    * To disable a specific warning, find the warning code from the list [here](https://seanwasere.com/pylint--list-msgs/) and add it to the list of disabled warnings. For example, to disable the message `[invalid-name] Constant name "XXX" does not conform to UPPER_CASE naming style`, first search the link for `invalid-name` to determine that the correct code is `C0103`, then add it to the list, as shown below
    
            disable=raw-checker-failed,
                bad-inline-option,
                locally-disabled,
                file-ignored,
                suppressed-message,
                useless-suppression,
                deprecated-pragma,
                use-symbolic-message-instead,
                C0103
                
    * To disable everything, change the entry to `disable=all`     
    
 4. Save your changes, **shutdown your Jupyter server** and then **login again**. When your server restarts, pylint should detect the changes and stop nagging you about your terrible code style ;-) 
    
    
