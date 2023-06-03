# chromeos_hax
A set of hacks I use to build chromeos


## Background

Chromeos is a well built os - but if you're a developer, you'll need a C compiler and other items that are unavailable in the OS. I don't like the idea of "Crostini" or needing to run a virtualized machine to run a real linux environment.

If you want to roll your own version of chromeos - See the chromiumos developer guide for more details

The repo doesn't contain many of  my scripts for security's sake as I run a trimmed down version.

## Installation

 - (inside chroot) add the script file to the chromite/scripts directory
 - symlink the script to "wrapper3.py" (all the binaries are symlinked)

## Scripts

 - remove_package_from_build.py -- I built this as it's suprisingly hard to remove an existing gentoo package from the chromeos source library without many hours of tedious crosschecking, especially if your package has a lot of reverse dependencies. This script gathers all the dependencies, and then iteratively prompts you for input as you try to remove(nuke) a package.
