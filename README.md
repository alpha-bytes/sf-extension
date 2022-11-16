# sf-extension

This package exports the base class extended by all [sf-extend](/sf-extend) extensions. `sf-extend` is a plugin for the `sfdx` and `sf` cli applications. All generated extensions include reference to this package.

In addition to the constructor, the base class provides the following functionality to extending classes: 

## Properties

### `forceOverwrite` 

When set to true (default) any changes to existing files will generate a prompt to the user providing options on how to handle the change. Extending classes can set this property to `false` to override this behavior as such: 

```js
// make sure to set during or prior to Yeoman's writing() phase
writing(){
    this.forceOverwrite = true;
    //...
}
```