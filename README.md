# PHP Mars Rover Tech Challenge

### NOTE: I used PHP7.4 because I have wamp with this version for now and can't upgrade it because some of application is setup there.

![copy `app`](app.png "copy `app`")

## Comments By The Developer [Sandip Limbachiya]

### Core Backend Challenge Comments

My approach was to ensure that I use object oriented programming principles.
Objects were created for both the Plateau and Rover with constructors and getters and setters.

I solved the problem of turning left and right through cardinal directions by declaring them in a numbered array which I could
then increment and decrement through using the array indexes. 

Turning right from the last element or left from the first is controlled for and the array effectively loops around to allow continuous turning.

Movement is done through simply incrementing or decrementing the x and y values depending on the current direction.
Movement is also restricted by the boundaries of the plateau and by any parked rovers.

### General Comments
1. The backend challenge was completed using PHP7.4.
2. I spent a bit of extra time for create test cases to make sure that everything is working as expected.
3. I did not use a framework like symfony for the backend as this would have been overkill for a project with a limited scope and lifespan.

### Example
As per our requirement (created test cases), Assuming a top right grid input of x = 5 and y = 5 and two rovers with the following data:

Rover 1: 
    X-Axis Start: 1 
    Y-Axis Start: 2 
    Direction: N
    Move Commands: LMLMLMLMM

Rover 2: 
    X-Axis Start: 3
    Y-Axis Start: 3 
    Direction: E
    Move Commands: MMRMMRMRRM

You could expect to see the two rovers end up in the following positions and directions:

Rover 1: 1 3 N

Rover 2: 5 1 E

### Prerequisites

A web server capable of running PHP

A modern web browser


### Installing

1. make a clone of this application.
2. run 'composer install' command in project directory to download third party vendor directory.
3. for test the requirement, run the test cases like using below steps.

## Running the tests

Test are run with [phpunit](https://phpunit.de/)

1. Open a terminal and navigate to the project root folder
2. Run the following command: `vendor/bin/phpunit --colors=always  tests/RoverTest.php`

Make a test using command line

1. Open a terminal and navigate to the project root folder
2. Run the following command: `php app/app.php`
3. add the input and can see the output like attached screenshot above.


## Authors

* **Sandip Limbachiya**
