# MySQL

## Installation

We will install [MySQL](http://www.mysql.com/) using Homebrew, which will also install some header files needed for MySQL bindings in different programming languages \(MySQL-Python for one\).

```text
$ brew install mysql
```

## Usage

To have launchd start MySQL now and restart at login:

```text
$ brew services start mysql
```

Or, if you don't want/need a background service you can just use the `mysql.server` tool:

```text
$ mysql.server start
```

To stop it when you are done, run:

```text
$ mysql.server stop
```

You can see the different commands available for `mysql.server` with:

```text
$ mysql.server --help
```

To connect with the command-line client, run:

```text
$ mysql -uroot
```

\(Use `exit` to quit the MySQL shell\)

**Note**: By default, the MySQL user `root` has no password. It doesn't really matter for a local development database. If you wish to change it though, you can use `$ mysqladmin -u root password 'new-password'`.

## GUI Tool

It is always nice to have a GUI tool for managing databases. For Mac, you can use [Sequel Pro](http://www.sequelpro.com/) to manage local and remote MySQL databases. It is a free tool, you can choose to donate to support the development.

You may install Sequel Pro using [homebrew](http://sourabhbajaj.com/mac-setup/Homebrew/Cask.html):

```text
$ brew cask install sequel-pro
```

