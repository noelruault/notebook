# Java

## Installation

First you should check if Java is already installed

```text
$ java -version
```

If you see an output like below then Java is already installed on your machine so skip to _Add Java to PATH_.

```text
java version "1.8.0_45"
Java(TM) SE Runtime Environment (build 1.8.0_45-b14)
Java HotSpot(TM) 64-Bit Server VM (build 25.45-b02, mixed mode)
```

If you don't see the output like above then you need to install Java on your system.

### Using the Oracle installer

Please download the macOS version from the [Oracle website](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).

### Using Homebrew

```text
brew update
brew tap caskroom/versions
```

Then, install latest version of Java 9 via:

```text
brew cask install java
```

or install Java 8 using:

```text
brew cask install java8
```

Check if Java is correctly installed by running the `java -version` command again.

## Add Java to PATH

Add `JAVA_HOME` to your environment variables by adding the line below to your `env.sh` \(see [iTerm2](https://github.com/noelruault/notebook/tree/b16c4e8eb0b5f4a9f73c68612c647df139d4daca/mac-setup/iTerm/README.html) section if you don't have a `env.sh` file\).

```text
export JAVA_HOME="`/usr/libexec/java_home -v 1.8`"
```

If you are using Java 9, use the following:

```text
export JAVA_HOME="`/usr/libexec/java_home -v 9`"
```

You should have Java working now. Two popular IDE alternatives for writing Java are [Eclipse](https://www.eclipse.org/downloads/) or [IntelliJ](https://www.jetbrains.com/idea/download/).

