# RELEASE HISTORY

## 1.2.1 / 2012-12-19

This release imporves the help output and manpage lookup
as well as a few helpful additions the the API.

Changes:

* Improve manpage lookup.
* Improve overall help output.
* Add alias_switch and alias_accessor helpers.


## 1.2.0 / 2012-01-31

Version 1.2.0 is complete rewrite of Executable. Actually it was decided that
the old design was too simplistic in it design concept, so another library
that was in the works, called Executioner, and briefly CLI::Base, was
ported over. And with some API changes, it is now the new Executable project.
The idea of the project is generally the same, but Executable now offers
more features, such as good help output and namespace-based subcomamnds.
Of course, to accommodate all this the API had to change some over
the previous version, so be sure to read the API documentation.

Changes:

* Deprecate old implementation.
* Port Executioner project over to become new Executable project.
* Supports namespace-base subcommmands.
* Supports formatted help output in plain text and markdown.
* Supports manpage look-up and display.


## 1.1.0 / 2011-04-21

This release simplifies Executable, removing the #option_missing method
and using the standard #method_missing callback instead. Along with this
the special error class, +NoOptionError+, has been removed. This release
also fixes an issue with inconsistent arguments being passed to the callback.
Finally it renames the #execute_command method to simple #execute!.

Changes:

* Name Changes

  * Renamed `#execute_command` method to `#execute!`.

* Deprecations

  * Rely on #method_missing callback instead of special #option_missing method.
  * The +NoOptionError+ exception class is no longer needed because of above.

* Bug Fixes

  * The #method_missing callback takes the value of the option being set.


## 1.0.0 / 2011-04-15

This is the initialize release of Executable (as a stand alone project).
Executable is a mixin that can turn any class into an commandline interface.

* 1 Major Enhancement

  * Birthday!

