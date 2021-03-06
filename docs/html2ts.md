#### Control generated TypeScript module and variable names

In the task options `htmlModuleTemplate` and `htmlVarTemplate` you can specify an Underscore templates to be used in order to generate the module and variable names for the generated TypeScript.

Those Underscore template receive the following parameters:

 * filename - The html file name without the extension ("test" if the file was named test.html)
 * ext - The html extension without the dot ("html" if the file was named test.html)

The default templates are:

 * "<%= filename %>" - for the module name. (This maintain existing behavior of older versions, and allow controlling the module name by simply renaming the file.)
 * "<%= ext %>" - for the variable name. (This maintain existing behavior of older versions, again allowing to control variable name by renaming the file.)

Usage example is setting the module template to "MyModule.Templates" and the variable template to "<%= filename %>" this will result for the test.html file above with the generated TypeScript
```typescript
module MyModule.Templates { export var test = '<div Some content </div>' }
```
