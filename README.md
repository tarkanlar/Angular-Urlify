angular-urlify
==============

Filter to create better seo urls and slugs with angularjs based on Django Urlify
https://github.com/django/django/blob/master/django/contrib/admin/static/admin/js/urlify.js

## Usage

Import `angular-urlify-filter.js` your AngularJS project and add `ngUrlify` to
your module as a dependency.

```
angular.module('myApp', ['ngUrlify']);
```

Then you can use the filter in your templates:

```
<p>Title: <input type="text" ng-model="title"></p>
<p>Urlized title: {{ title | urlify }}</p>
```

Also you can use it in your javascript code:

```
app.controller('TestController', ['urlifyFilter', function (urlify) {
    $scope.urlizedTitle = urlify('Your text');
}]);
```

