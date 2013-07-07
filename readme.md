How to release
==============

* Download the version of 'IronPython Binaries' you want to release
* Unzip in `package\tools` dir
* Update `<package><metadata><version>` in file `package\Package.nuspec` accordingly
* Run `NuGet.exe pack package\Package.nuspec`
  * You should see many warnings 'Assembly outside lib folder', they are normal
* Test that the package work as expected by running `NuGet.exe install IronPython.Interpreter -Source C:\path\to\generated\nupkg`
* Run `NuGet.exe push IronPython.Interpreter.X.Y.Z.nupkg`
