# Authentication via GitHub

 1. Create a personal access token following the steps described [here](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)
 2. Using VSCode, create a file in your `$HOME` directory called `.git-credentials`
 3. Add the following line to the file

        https://YOUR_GITHUB_USERNAME:YOUR_PERSONAL_ACCESS_TOKEN@github.com
        
 4. From a terminal, run `git config --global credential.helper store` 
