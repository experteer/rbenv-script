# rbenv-script

This is a plugin for [rbenv](https://github.com/sstephenson/rbenv)
that lets you execute scripts before spawning Ruby processes.

The code is heavily based on Sam Stephenson's [rbenv-vars](https://github.com/sstephenson/rbenv-vars). 

## Installation

To install rbenv-script, clone this repository into your
`~/.rbenv/plugins` directory. (You'll need a recent version of rbenv
that supports plugin bundles.)

    $ mkdir -p ~/.rbenv/plugins
    $ cd ~/.rbenv/plugins
    $ git clone https://github.com/experteer/rbenv-script.git

## Usage

Puts scripts to be executed an `.rbenv-script` file in your project.
For example:

 export RUBY_GC_MALLOC_LIMIT=50000000
 

The `~/.rbenv/script` file will be executed
first. Then `.rbenv-script` then `.rbenv-script.local` in any parent
directories of the current directory will be executed. `.rbenv-script` then 
`.rbenv-script.local` in the current directory are executed last.

Use the `rbenv script` command to print the complete script to be executed.

## Version History

**0.0.1** (February 5, 2014)

* First release

&copy; 2014 Peter Schrammel. Released under the MIT license. See
`LICENSE` for details.
