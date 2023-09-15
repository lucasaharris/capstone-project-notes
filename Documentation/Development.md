# Linting
* Steps for linting Ruby code:
  * install rubocop gem: `gem install rubocop`
  * to lint the project simply type `rubocop` in your terminal
    * you should see a list of violations as output
  * to automatically correct the offenses run `bundle exec rubocop --autocorrect`
* Steps for linting JavaScript code:
  * To get started, run the following command in the terminal to install ESLint as a dev dependency:
    * `npm install --save-dev eslint eslint-config-airbnb`
  * Then initialize ESLint.
    * `npx eslint --init`
  * You’ll be prompted with questions about your project. When prompted with:
    * `? How would you like to use EsLint?`
  * Select this option:
    * `To check syntax, find problems and enforce code style`
  * Answer the next questions as per your project until you come across the following prompt.
    * `? How would you like to define a style for your project?`
  * Answer:
    * `Use a popular style guide`
  * Select the Airbnb style guide for the next prompt.
    * `<? Which style guide do you want to follow? \n > Airbnb: <https://github.com/airbnb/javascript>`
  * Lastly select "Yes" to install the required dependencies.
  * There should now be a .eslintrn.json file in the root of the folder.
  * To run the linter on a js file use:
    * `npx eslint [relative path to file]\file.js`
* To lint embeded JavaScript in an html file simply add the following to your .eslintrn.json file:
  * `plugins: [
    "html"
  ]`
  * To run the linter on an html file with embeded js use:
    * `npx eslint [relative path to file]\file.html`
 
# Environment Setup

## Replicating via Docker
* Clone the repo
   * In your terminal: `$ git clone https://github.com/ahuelhorst/documentor.git`
* If you do not already have Docker installed on your machine, do so through https://docs.docker.com/get-docker/ and create an account
* Open and run the Docker Desktop app on your machine
* Type `docker-compose build` in your terminal in the root of the project
* Type `docker-compose up` in your terminal in the root of the project
* You should see  "* Listening on http://0.0.0.0:3000" once the images are ready and running
* Open the link in your browser
    * The first time running the image you will have to resolve pending database migrations
        * To do so: after you have opened the link in your browser, scroll to the bottom of the page and click "run pending migrations"

## Manual set up
  ### Install prerequisites (MacOS)
  1. Install Homebrew if not already installed
  * Type the following command into your terminal: `$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
  * Enter your mac password (used to sign in to your device) when prompted
  * Verify installation with: `$ brew doctor`
     * if installed, output should be: `Your system is ready to brew`
     * if you see `zsh: command not found: brew` type the following into your terminal and then restart terminal: 
       * `$ echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile`
       * `$ eval "$(/opt/homebrew/bin/brew shellenv)"` 
       
  2. Install Ruby
  * Install rbenv
     * Type the following commands into your terminal:
       * `$ brew install rbenv`
       * `$ rbenv init`
       * `$ echo 'eval "$(rbenv init - )"' >> ~/.zshrc`
       * restart your terminal for changes to take effect
   * Install ruby
     * Type the following commands into your terminal: 
       * `$ rbenv install 2.7.5`
       * `$ rbenv global 2.7.5`

   3. Install shared-mime-info: `$ brew install shared-mime-info`
 
   4. Install Rails: `$ gem install rails -v 6.1.3`
   
   5. Install PostgreSQL: `$ brew install postgresql`
   
   6. Install node js: `$ brew install node`

   7. Install yarn: `$ npm install --global yarn`
   
 
   ### Install prerequisites (Windows)
   1. Install NodeJS
   * go to https://nodejs.org/en/ and download the latest stable version
   * run the installer: <u>node_versionnumber.msi</u> and follow the instructions
   2. Install Yarn
   * run `npm install --global yarn` in terminal
     * or
   * go to https://classic.yarnpkg.com/en/docs/install#windows-stable and download the latest stable version
   * run the installer: <u>yarn_versionnumber.msi</u> and follow the instructions
   4. Download SQLite3
   * go to https://sqlite.org/download.html and scroll to the section titled "Precompiled Binaries for Windows"
     * download the <u>sqlite-tools-win32-x86-versionnumber.zip</u> file and extract the files to <i>..\Windows\System32</i>
     * download the <u>sqlite-dll-windowsversion-versionnumber.zip</u> file that matches your version of Windows and extract the files to <i>..\Windows\System32</i>
   5. Install Ruby
   * go to https://rubyinstaller.org/downloads/archives/ and download <u>rubyinstaller-devkit-2.7.5-1-x64.exe</u>
     * run the installer and follow the instructions
   6. Install SQLite3: type <strong>gem install sqlite3</strong> in your terminal
   7. Install Rails: type <strong>gem install rails</strong> in your terminal
   8. Install PostgreSQL
   * go to https://www.enterprisedb.com/downloads/postgres-postgresql-downloads and download the latest version under "Windows x86-64"
     * run the installer and follow the instructions
   9. Install Graphviz
   * go to http://graphviz.org/download/ and scroll down to the Windows section, and choose the latest version that matches your OS
   * run the installer: <u>windows_10_cmake_Release_graphviz-install-versionnumber-OSversion.exe</u>, and follow the instructions
     * once it is installed, go to your terminal and type <strong>`pip install graphviz`</strong> and let the installation finish
   10. Check that each program installed correctly
   * Ruby: <strong>`ruby --version`</strong>
   * SQLite3: <strong>`sqlite3 --version`</strong>
   * NodeJS: <strong>`node --version`</strong>
   * Yarn: <strong>`yarn --version`</strong>
   * Gem: <strong>`gem --version`</strong>
   * Rails: <strong>`rails --version`</strong>
   * PostgreSQL: navigate to <i>..\PostgreSQL\15\bin</i> and run <strong>`postgres --version`</strong>
   
   ## Clone the repo
   * In your terminal: `$ git clone https://github.com/ahuelhorst/documentor.git`
   * **This repo is currently private as it is a clone of DocuMentor's documentor repo**

   ## Set up PostgreSQL db
   * Start postgres server (via brew on mac): `$ brew services start postgresql@14`
   * Log in: `psql -U 'username'`
   * Create a new database: `create database 'dbname'`
  
   ## Set up project
   * In your cloned repo:
      * Run `$ bundle install` 
      * Run `$ bin/setup`
        * on Windows: `ruby bin/setup`
      * MacOS: Run `$ yarn install`
      * Create a .env file in the root of the project following the .env.example file
        * <strong>This is where you will specify postgres username, password, access keys etc.</strong>
      * To set up tables run: `$ rails db:migrate`
      * To add the data to the database: `$ rails db:seed`
      * To populate tables with test data run:  `$ rails dev:prime`
  
  
  ## To run the project (locally)
  * Start your postgres server: `$ brew services start postgresql@14` (on mac)
  * Run `$ rails s` (in the root of your project)
      * After typing this command you should see something like: "* Listening on http://127.0.0.1:3000"
  * Open the link in your browser


  ## Troubleshooting
  * After following environment set up: 
    * (Windows Specific) If you encounter an "Invalid URI" error when trying to run `ruby bin/setup`, run the following commands one after the other             instead of running `ruby bin/setup`: 
      * `ruby bin/rails db:prepare` 
      * `ruby bin/rails log:clear tmp:clear` 
      * `ruby bin/rails restart` 
     * If you encounter a Webpacker compilation error, check your version of Node (`node --version`). If you have node version 17 or above, downgrade your      version to 16.18.0
     * env file issue: If you are using DocuMentor's .env file (need permission, not provided in our repo) and you recieve a "Invalid password for                user..." error, ensure that you have created a role in postgres with DocuMentor's exact 'RDS_USERNAME', 'RDS_PASSWORD', and 'RDS_DB_NAME'. 
       See the following postgres commands for guidance: 
          * `CREATE ROLE <RDS_USERNAME> SUPERUSER LOGIN PASSWORD <RDS_PASSWORD>;`
          * `GRANT USAGE ON DATABASE <RDS_DB_NAME> TO ROLE <RDS_USERNAME>;`
   * When trying to log in to DocuMentor's login page:
       * if username 'employee1@example.com' and password 'password' do not work and you are given a "Invalid Email or password" message, run the                  following commands in your project's terminal and then try to log in again:
            * `rails db:seed`
            * `rails db:prime`'
   
  
  # Tests
  * to javascript run tests: `yarn test`
     * to run tests for a specific file: `yarn test <file name>`
     * add `--coverage` to generate a coverage report
  * to run ruby tests: `rspec <file name>`
 





   



  
 
  
  

  
 
  
  
  
   
    
   
   
   


  
  
