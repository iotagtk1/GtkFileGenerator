### GtkFileGenerator

Generates a new template file generated by GtkSharp.Template, renaming the class.
Template.
It is convenient to use external tool registration in Rider.

#### Usage
- install GtkSharp.Template.CSharp or install gtkSharp from Nuget 
- Copy and paste the class name.
- Set the arguments to GtkFileGenerator
- Run the GtkFileGenerator

#### Location of the GtkSharp template file

https://github.com/GtkSharp/GtkSharp

The templates can be installed from dotnet new.

#### nuget gtkSharp

https://www.nuget.org/packages/GtkSharp/

```
$ dotnet new --install GtkSharp.Template.CSharp
```

#### Run from a terminal

Run from a terminal You can't use macros in a terminal, so you need to put the absolute path in the projectDir.

```
$ GtkFileGenerator -projectName namespace name -projectDir projectPath
```

##### Run from Rider macro can be used

Settings - Tools - External Tools

Register this app with external tools.

Set the path of the program.
Set the arguments.

```
-projectName $SolutionName$ -projectDir $FileDir$
```

The working Path can be empty.

Uncheck the "Synchronize after execution" box.

When you run the GtkFileGenerator, a class file based on the template file will be generated in the project folder.

#### Modify the templates at 

Modify classTemplate.txt and gladeTemplate.txt.

#### If you cannot build 

When importing with Rider, please re-set the file properties to Embeded resource.
Or use AddItem to add it again.