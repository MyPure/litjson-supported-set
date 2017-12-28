LitJSON
=======

[![Build status](https://ci.appveyor.com/api/projects/status/ciq9vo4caq0wmxap/branch/develop?svg=true)](https://ci.appveyor.com/project/litjson/litjson/branch/develop)

A *.Net* library to handle conversions from and to JSON (JavaScript Object
Notation) strings.

[Project website][litjson].


## Compiling

See the files under the `build` directory.

### Using GNU Make

Change directory to `build/make/` and run `make` from it. This tries to use
the `gmcs` compiler by default. Feel free to open the `Makefile` and tweak
it according to your needs.

### Using other tools

Currently, LitJSON doesn't have any other auxiliary files for compiling this
library with other tools.

If you want to contribute your own solutions to compile it with tools like
*NAnt* or *MSBuild*, that would be most appreciated. Please create those
auxiliary files under the path `build/some-tool`. Thanks.

## Tests

This library comes with a set of unit tests using the [NUnit][nunit]
framework.

If you have [pkg-config][pkg-config] in your system, and the *Mono* suite
provides the `mono-nunit.pc` file, you can try running these tests by running
`make test` from the `build/make` directory.

You can specify which `pkg-config` is invoked by passing a `PKG_CONFIG`
variable to `make test`. This is useful when you have mutiple conflicting
`pkg-config`s on your system and need to select the correct one (i.e. to
avoid conflicts with Homebrew on Mac OSX).

Example of running the tests on Mac OSX:

```bash
# In litjson/ directory
$ cd build/make
$ make PKG_CONFIG=/Library/Frameworks/Mono.framework/Commands/pkg-config test
```

## Using LitJSON from an application

#### Package manager

```PowerShell
Install-Package LitJson -Version 0.9.0
```

#### .NET CLI

```PowerShell
dotnet add package LitJson --version 0.9.0
```

#### Paket CLI

```PowerShell
paket add LitJson --version 0.9.0
```


Alternatively, just copy the whole tree of files under `src/LitJSON` to your
own project's source tree and integrate it with your development environment.

## License

[Unlicense][unlicense] (public domain).


[litjson]: [unlicense](http://unlicense.org/
[nunit]: http://www.nunit.org/
[pkg-config]: http://www.freedesktop.org/wiki/Software/pkg-config
[unlicense]: http://unlicense.org/
