## ForEach Statement

A `foreach` statement takes a function and runs it on each item in an array.

```javascript
 array.forEach(function(argument);
 ```

Here it is, in use, with an array called `elevators` and a function called... `function`.

 ```javascript
 function(elevators, floors) {
  elevators.forEach(function(elev){
    elev.on("floor_button_pressed", function(floorNum) {
      elev.goToFloor(floorNum);
    })

    elev.on("idle", function(floorNum) {
      elev.goToFloor(0);
    })               
  });
}
 ```



 (Thanks to [The Elevator Saga](http://play.elevatorsaga.com/) for today's TIL.)
