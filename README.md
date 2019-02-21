After seeing your review of their Automail simulation design, ABC Company were
outraged and sought revenge. They organised to have you kidnapped, and abandoned in a dangerous location,
with the expectation that you would not survive your attempt to return to civilisation.
Awaking in a strange vehicle in an unfamiliar location surrounded by dangerous traps, you quickly realised
that attempting to drive out manually would soon prove fatal. However, ABC did not account for your
software design and development skills. You quickly connected your laptop (conveniently left with you) to
the vehicle, coupled it with the vehicles sensors and actuators, and integrated your tailor-designed vehicle
auto-drive system. In no time at all (well, before the due date at least) you were on your way, the vehicle
automatically navigating its way across the map to safety, as quickly as possible*, while avoiding+ the traps.

The Map

The area you find yourself in is a constructed in the form of a simple grid of tiles consisting only of:
* Roads
* Walls
* Start (one only)
* Exit
* Traps
Some roads may lead to dead-ends or be impassible due to traps.

The Vehicle

The car you find yourself in includes a range of sensors for detecting obvious properties such as the car’s
speed and direction, and actuators for accelerating, braking and turning. It has a maximum speed (which is
slower in reverse) and a limited turning rate. The car also includes a sensor that can detect/see four tiles in
all directions (that’s right, it can see through walls), ie. a 9x9 area around the car. The car can be damaged
by events such as running into walls, or through traps (see below). It has limited health; if the car’s health
hits zero, ABC wins and you lose. Similarly, if the car is stuck in a trap and can’t continue, you lose. If
however, your software takes the car from the start to the exit, you win and live on to write more damning
software design reviews.
*The time it takes the car to reach the exit and the final health of the car will be combined to provide a score
for your escape.

The Traps

There are different types of traps which have different effects on your vehicle; the effect continues as long as
the vehicle is in the trap:
* Lava: damages your vehicle.
* Mud: slows your vehicle down.
* Grass: causes your vehicle to slide (no change in direction is possible).
A lava trap may destroy your vehicle and a mud trap may stop and hold your vehicle, either way resulting in
failure. A grass trap is not a problem in its own right, but where you end up when you leave the grass trap
may be a problem.
+ Some traps will be avoidable (i.e. can be by-passed), but others will have to be traversed with some
consideration as to the resulting damage and to where the car ends up.

The Task

Your task is to design, implement, integrate and test a car autocontroller that is able to successfully traverse
the map and its traps.
It must also be capable of:
1. planning a route
2. updating the route in the presence of roads which can’t be traversed due to traps
3. traversing traps if necessary, and safe to do so

A key element is that your design should be extensible to allow the implementation to be changed in the
future to deal with other trap types, arrangements of traps, and additional or faster traversal strategies (see
Design Rationale below). You will not be assessed++ on how sophisticated or fast-traversing your algorithms
are, beyond whether they work to get the car to the exit (++other than for the bonus mark for the top 5%
based on total score).

The package you will start with contains:
* The simulation of the world and the car
* The car controller interface
* A car manual controller that you can use to drive around a map
* A working but basic car autocontroller that can navigate a maze but ignores traps and can stuck in a
circuit if the map is not a ‘perfect maze’ (no loops).
* Sample maps (created using the map editor Tiled)
