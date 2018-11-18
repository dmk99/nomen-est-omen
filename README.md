# Nomen est Omen

![](https://img.shields.io/maven-central/v/com.oblac/nomen-est-omen.svg)

_"Your name is your destiny"_, so be sure you pick a good name.
This Java library helps with generating some super-awesome random names
that you can use for some unique IDs :)

Generated names may consist of:

+ adjective (70+ names)
+ color name (50+ names)
+ person name (140+ names)
+ superb name (10+ names)
+ pokemon name (700+ names)
+ count (any number > 0)

For example, you can get names such: `hungry_navy_babbage`
or `dreamy_cray`. Isn't this super great?

## Changes

* Compiled for Java 1.8

## Usage

It's complicated.

### 1. Add dependencies

In your Gradle or Maven project, add:

    com.oblac:nomen-est-omen:<version>

### 2. Use it

If you just want a short name (adjective and person name):

	Nomen.randomName();

If you want to build your own template, e.g.:

	Nomen.est().adjective().color().person().get();

Variables are set using `withXxx()` methods:

	Nomen.est().adjective().color().person().withCount(3).get();
	
That is all.

### 3. Optimise

Templates can be created once:

	Nomen uigen = Nomen.est().adjective().person();
	...
	String id1 = uigen.get();
	String id2 = uigen.withCount(7).get();

Nice!

## Thanx to Docker

I am blatantly stealing idea from [Docker](https://github.com/docker/docker/blob/master/pkg/namesgenerator/names-generator.go).
It is so beautiful, that it deserves Java port :)


## License

[BSD](LICENSE)