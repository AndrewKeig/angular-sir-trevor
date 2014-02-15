#angular-sir-trevor

Allows you to inject sir-trevor into Angular controllers and services


## Install

Run the following bower command to install

```
bower install angular-sir-trevor
```

Now add angular-sir-trevor script to your index.html page

```
bower_components/angular-sir-trevor-js/angular-sir-trevor.js
```


Now add the dependency to your main angular app

```
angular.module('app', ['sirtrevor'])
```


## Usage

In order to use sir-trevor you can simply refer to it in your controllers like so

```
angular.module('app')
.controller('MainCtrl', function ( $window, sirtrevor) {
```

Now we have this setup we can go ahead and create a sirtrevor editor, and assign it to window.editor; which we also inject.

```
$window.editor = new sirtrevor.Editor({
    el: $('.sir-trevor'),
    blockTypes: [
      "Heading",
      "Text",
      "List",
      "Quote",
      "Image",
      "Video",
      "Tweet"
    ]
  });
 ```