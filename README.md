# ModSimProject3
Inspired by the famous scene in the movie, Indiana Jones and the Raiders of the Lost Arc, we set about to discover the optimal slope needed to slide a mass from the top of a hill to the position of a hapless grave robber, while taking drag and friction into account. We found that a slope of -1.79 gets the mass in question from point A to point B in 1.97 seconds, faster than any other.

![pic](https://github.com/minhkhang1795/ModSimProject3/blob/master/media/pic.jpg)

## The Question

In order to protect the secrets hidden within the ancient crypts, you are building a trap that involves a large mass of stone sliding down an inclined plane, and towards a hapless intruder. Assuming that point A, the point from which the block is dropped, is 10 meters above the ori gin, and point B, the position of the intruder, is 10 me ters to the right, what slope of the plane gets the object from point A to point B the fastest?

![fig1](https://github.com/minhkhang1795/ModSimProject3/blob/master/media/fig1.PNG)

## The Brick, Mathematically

As the brick itself is the moving part in question, many
components of the system depend on the traits we as
signed to it. For the purpose of the simulation, we gave
the brick dimensions of a 0.15m cube, and assigned it a
mass of 6.48 kg. We found that the coefficient of drag
on a cube is 0.8, and the coefficient of friction between
the brick and the ground, which we decided was made of
wood, is 0.6.

![free-body-diagram](https://github.com/minhkhang1795/ModSimProject3/blob/master/media/free-body-diagram.PNG)

In order to simulate this model, we defined a few key
points. The force of gravity was determined with the
gravitational constant (g) and he slope of the hill (θ).
Friction was calculated using gravity, the slope of the hill
and the coefficient of friction (μ). Drag was determined
by the density of air (ρ), object velocity (v), coefficient
of drag (Cd), and the surface area of a single side (A).


![math](https://github.com/minhkhang1795/ModSimProject3/blob/master/media/math.PNG)

## Initial Validation

In order to make sure our model worked accuratly,
we first tracked the position of the brick, without
friction and drag, as it traveled down a single de
fined slope.

Once we had gotten a reasonable output we com
pared it against hand calculations to make sure our
model matched the actual physics. We then added
in drag and friction while making sure the results
remained plausible. We then manually tested a few
points between -5 and -1 before finally sweeping
through all slopes within our previous boudaries.

![fig2](https://github.com/minhkhang1795/ModSimProject3/blob/master/media/fig2.PNG)

After sweeping through possible slopes, we plotted our results against the duration of the time it took for the brick to travel from point A to point B. We found the op timal slope of a brick cube traveling down a wooden in cline plane to be -1.79. Using this slope it took the brick 1.97 seconds to travel down 10m and right 10m. We found that the shortest past is not nessesarily the fastest when dealing with gravity, friction and drag.

![fig4](https://github.com/minhkhang1795/ModSimProject3/blob/master/media/fig4.PNG)

## Simplifications

The real world is never perfect, and because of this, we
must make a few generalizations about the situation.

* The simulation uses a single, constant coefficient of
friction.
* While the situation we are modelling likely has a curve,
our model does not. We account for this by ensuring
that velocity is conserved from the slope to the hori
zontal plane.
* We are modeling a situation where the brick in question
is perfectly flat, with no surface imperfections.
* We set the air density and force of gravity equal to that
at sea level.
* We are using rough approximations for the drag coeffi
cient of a cube, and for the coefficient of friction for
brick on wood.

![fig5](https://github.com/minhkhang1795/ModSimProject3/blob/master/media/fig5.PNG)

## Limitations

* We only model two dimensions, removing the chance of
moving along the z-axis, as a three-dimensional object
would.
* As the results are only tested with equivalent rise and
run, the optimal slope could be different under different circumstances.
* The model fails to account for variations in the coefficient of friction that occur as material, humidity, and
other similar variables change.

## Future Steps

Though our simulation came up with an answer, there
are many possible improvements we could make, including:
* Using a round object rolling down a linear ramp,
which would involve including rotational physics
* Finding the optimal curve between two points
* Including a person running away from the sliding brick
to bring our model closer to reality

## Built With

* [Jupyter Notebook](http://jupyter.org/)
* Python 3

## Authors

* Kyle Bertram
* Khang Vu
* Mika Notermann

## Acknowledgments

* [ModSimPy](https://github.com/AllenDowney/ModSimPy) by Allen Downey
