# Setting Up Development Environment

## Java Developer Kit 8 (JDK8)
  Download latest version of JDK from Oracle.

  [download here](https://www.oracle.com/technetwork/java/javase/downloads/index.html), Find Java SE 8uxxx and download JDK.

## Maven
  Go to [Maven Official website](http://maven.apache.org/download.cgi) download an binary archive and add to `PATH`
  1. On Windows:
    - View advanced system settings (through search or control panel)

    - Go to Advanced tab and click on Environment Variables

    - Find `Path`, click on **edit**, then click on **New**.

    - add the `bin` directory to the path. Path example: `C:\Program Files\apache-maven-3.6.0\bin`

    **NOTE**: Users with [Chocolatey](https://chocolatey.org/) and run `choco install maven`

  2. On Mac:

  Unzip the file and add the `bin` directory to `PATH`. To permenantly change the path variable: change `your_user_name\bash_profile`. Add a line:`export PATH={your Maven directory}/bin:$PATH`

  User with homebrew: `brew install maven`

  3. On Linux: `sudo apt-get install maven`

## Set Up Heroku
  1. create a free account [here](https://www.heroku.com/)
  2. install Heroku CLI: https://devcenter.heroku.com/articles/deploying-spring-boot-apps-to-heroku

## Set Up Spring Boot
  Install the Spring CLI as described in the [documentation](https://docs.spring.io/spring-boot/docs/current/reference/html/getting-started-installing-spring-boot.html#getting-started-installing-the-cli).

  - On Mac:
  ```bash
  $ brew tap pivotal/tap
  $ brew install springboot
  ```
  If you don't have brew, then install with `$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)`

  - On Windows: Install with [Scoop](https://scoop.sh/)
  ```bash
  > scoop bucket add extras
  > scoop install springboot
  ```
  Scoop installs `spring` to `~/scoop/apps/springboot/current/bin`.

## Spring Tool Suite
  Install from [here](https://spring.io/tools/sts/all). Select according to your operating system.

## Node.js
  1. Windows:

    - Download the windows installer for Node.js from the [Node.js website](https://nodejs.org/en/)

    - Run the installer (the .msi file downloaded in Step 1)

    - Accept the license agreement and all defaults and click install.

  **Test the installed packages** (Restart your computer)

  **Test Node**: open command prompt and type node -v .

  **Test NPM**: In command prompt, type npm -v.

  2. Mac:
  ```bash
  $ brew install node
  ```
  **Test the installed packages** (Restart your computer)

  **Test Node**: open command prompt and type node -v.

  **Test NPM**: In command prompt, type npm -v.

## MongoDB:
  Install mongodb from [here](https://docs.mongodb.com/manual/installation/)
  1. Windows:
    - Download the windows installer for MongoDB from [MongoDB Download Center](https://www.mongodb.com/download-center/community?_ga=2.235666241.1559492448.1525556338-1618931155.1525556338)

    - Run the installer (the .msi file downloaded in Step 1)

    - Accept the license agreement and all defaults and click install. You may install MongoDB in any folder (For example: C:\Program Files\).

    - Create a directory named “db” using the command `> mkdir \data\db` All the Mongo data files will be saved to this directory. Make sure this directory has write permissions

    - Add bin to Environment PATH
  2. Mac: `brew install mongodb`

  Operate MongoDB with [manual](https://docs.mongodb.com/manual/)

  **Start a Mongo Server**: `mongod --dbpath={your db path} --port={your port usually 27100}` example: `mongod --dbpath=C:\mongodb\db --port=27100`

  **Connect to MongoDB**: `mongo --port=...`