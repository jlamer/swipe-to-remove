angularApApp
============

it works, a lot of code borrowed from ngSwipe
uses ngTouch's swipe method,
needs a css class defined called moving to handle snap in place animation,
example uses ngAnimate to animate removal of items.

working plunkr demo
http://plnkr.co/edit/f8LgOJm3UanOdd559LM8?p=preview

to run demo install dependencies
```
cd demo
npm install
bower install
```
run the server
```
grunt server
```

Usage
in HTML
```
<div item-swipe on-remove="removeThing(thing)" ng-repeat="thing in things">{{thing.name}}</div>
```

in controller
```
$scope.removeThing = function(thing){
  $scope.things.splice($scope.things.indexOf(thing), 1);
};
```

in css

```
.moving {
  transition : all 0.2s ease-in-out
}
```

