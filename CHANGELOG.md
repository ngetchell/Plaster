# Plaster Release History

## 1.1.0
### Added
- Added constrained runspace cmdlet: Out-String [#235](https://github.com/PowerShell/Plaster/issues/236).
- Added constrained runspace variables: PSVersionTable and on >= PS v6 IsLinux, IsOSX and IsWindows [#239](https://github.com/PowerShell/Plaster/issues/239).
- The parameter element now supports a condition attribute so that prompting for parameters can be conditional based on environmental factors (such as OS) or answers to previous parameter prompts.  This allows you to build a "dynamic" set of prompts.
### Fixed
- Fixed prompt errors when prompt text null or empty [#236](https://github.com/PowerShell/Plaster/issues/236).

## 1.0.1 - 2016-12-16
### Fixed
- Fixed issue with the used of `GetModule -FullyQualifiedName` on PowerShell v3

## 1.0.0 - 2016-12-16
- First official release shipped to the PowerShell Gallery!

## 0.3.0 - 2016-11-05
- Updated build script with support for building help from markdown files, building updatable help files and generating file catalog.
- Initial release shows the basics of what this module could do.

## 0.2.0 - 2016-07-31
- Introduced new directive `<templateFile>` that implicitlys expands the specified file(s), allowing the
  template author to set the target file encoding.  This new directive supports a wildcard source specifier
  like the `<file>` directive.  With this change, `<file>` no longer supports template expansion and as result
   the `template` and `encoding` attributes have been removed.
- Restructured the module source to follow best practice of separating infrastructure from module files.
- Fixed #47: How to create empty directories.  The `<file>` directive supports this now.
- Fixed #58: File recurse does not work anymore.
