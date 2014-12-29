Ionic Contrib: Swipeable Cards
===================

Swipeable card based layout for Ionic and Angular. As seen in apps like [Jelly](http://jelly.co/)

[Demo](http://codepen.io/ionic/pen/nxEdH)

## Usage

Include `ionic.tdcards.js` after the rest of your Ionic and Angular includes. Then use the following AngularJS directives:

```html
<td-cards>
  <td-card ng-repeat="card in cards"
       on-destroy="cardDestroyed($index)"
       on-swipe-right="cardSwipedRight($index)"
       on-swipe-left="cardSwipedleft($index)">
    Card content here
  </td-card>
</td-cards>
```

To add new cards dynamically, just add them to the cards array:

```javascript
$scope.cards = [
  { // card 1 },
  { // card 2 }
];

$scope.cardDestroyed = function(index) {
  $scope.cards.splice(index, 1);
};

$scope.cardSwipedRight = function(index) {
  var newCard = // new card data
  console.log('card swiped right');
  $scope.cards.push(newCard);
};

$scope.cardSwipedLeft = function(index) {
  var newCard = // new card data
  console.log('card swiped left');
  $scope.cards.push(newCard);
};
```



