# Linear
Basic python support for linear algebra.
## Functionality
Some basic linear algebra concepts.
## Note
Only supports R^2 space for now.
### Point
Initialise by calling ```Point(x, y)``` where x and y are the coordinates.
Represents a point in R^2 space.
#### Methods and Properties
##### Point.x
The x coordinate.
##### Point.y
The y coordinate.
##### Point.coord
A string representing the vector in (x, y) format.
##### Point.asList
Returns the Point object as a list in the format [x, y].
### Line
Initialise by calling ```Line(a, b)``` where a and b are Point objects representing the start and end point of the line.
#### Methods and Properties
##### Line.a
Point A of the line.
##### Line.b
Point B of the line.
##### Line.coord
Start and end points of the line in ((x, y), (x, y)) format.
##### Line.midpoint
Returns a Point object that is the midpoint of the line.
##### Line.gradient
Returns a float that is the gradient of the line.
**NOTE**: gradient may be undefined.
##### Line.pgrad
Returns a float that is the gradient of a line perpendicular to the line.
**NOTE**: gradient may be undefined.
##### Line.edist
Returns a float that is the length (or euclidean distance) of the line.
##### Line.mdist
Returns a float that is the Manhattan (or block) distance of the line.
##### Line.lineEqn()
Returns a string that is the equation of the line in "y = mx + c" format.
**NOTE**: may be in "y = c", "y = mx", "y = mx + c" or "y = mx - c" format.
### Vector
Initialise by calling ```Vector(x, y)``` where x and y are the coordinates of the vector.
Currently, this is the only way to create a vector, although I plan to add a way to add a Vector object in terms of other Vector objects.
#### Methods and Properties
##### Vector.x
The x coordinate.
##### Vector.y
The y coordinate.
##### Vector.coord
A string that is the coordinate of the vector in "(x, y)" format.
##### Vector.length
Returns a float that is the length of the vector or ||v|| where v is the vector.
##### Vector.asList
Returns the Vector object as a list in the format [x, y].
##### Vector.term(v, w)
Returns a tuple (a, b) where a and b are from the format "K = aV + bW" where K is the Vector object, V and W are the other two vector objects and a and b are scalars. This function is used to express the vector in terms of other vectors.
##### Vector.smult(s)
Returns a Vector object that is the product of the scalar s and the Vector object.
##### Vector.vadd(v)
Returns a Vector object that is the sum of the Vector object and the other Vector v.
##### Vector.vsub(v)
Returns a Vector object that is the difference of the Vector object and the other Vector v.
##### Vector.dprod(v)
Returns a float that is the dot product of the Vector object and the other Vector v.
##### Vector.angle(v)
Returns a float that is the angle between the Vector object and the other Vector v.
##### Vector.scom(v)
Returns a float that is the scalar component of the Vector object in the direction of the Vector v.
#### Constants
##### VectorConstants.unitx
Returns a Vector object that is the unit x vector (aka <1,0>)
##### VectorConstants.unity
Returns a Vector object that is the unit y vector (aka <0,1>)
### Polygon
Initialise by calling ```Polygon([points...])``` where points is an array of Point objects (at least 3) that are the vertices of the object.
Will throw a InvalidPolygonError if less than 3 points are given.
Make sure the vertices are in anticlockwise order.
#### Methods and Properties
##### Polygon.vertices
The vertices of the polygon in anti-clockwise order. A list of Point objects.
##### Polygon.area
The area of the polygon.
##### Polygon.centroid
The centroid of the polygon as a Point object.
## Errors
### InvalidPolygonError
You entered less than three vertices when initialising a Polygon object.