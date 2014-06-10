XNA Content Compiler

This is very similar to this:

https://github.com/xupefei/XNA-4.0-Content-Compiler

except the code is refactored to be a little cleaner (IMO) and I've added
in command line functionality so you can use it via build scripts like rake 
or whatever you enjoy using.

USAGE:
  * build (Input Directory) (Output Directory)
    Builds all files in the input directory and places them into the output directory

  * build-file (Input File) (Output File)
    Builds a file and outputs it to the output file
    
  * watch (Input Directory) (Output Directory)
    Watches a directory for file changes and rebuilds changed files 

  * help
    Prints each command and a description

There are a few caveats here, namely the watch command isn't implemented yet
and anything ending with .xml, .ini or .config gets 1 to 1 copied from the 
input to the output directory. This is because I personally like using flat 
text files in some of my projects and don't want to have to copy them manually.

Lastly, since this uses MSBuild I couldn't get it to build on Mono or run in XBuild.
This makes it tricky to use on things like Linux based build servers.

If you want to take a stab at implementing the file watch stuff, be my guest and submit
a pull request.
