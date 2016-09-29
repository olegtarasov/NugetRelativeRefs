# NugetRelativeRefs
This package that makes all Nuget references in your project relative to $(SolutionDir)\packages folder. 
This is useful when you reuse single project in different solutions which don't reside in the same directory.

In order for this to work, just install the package into the project you want to reuse. Special Msbuild task
will transparently convert all package references to a relative format. This is done only for the duration of
the build, original project file remains unmodified. Thanks to this you don't need to do anything after you
update your packages.