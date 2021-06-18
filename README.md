# MetricTree

MetricTree is a tiny C++ library for organizing hierarchically a cloud of points in 
an arbitrary metric space.
It is similar to quad- and oct-trees with two differences :
there is no assumption on the geometric dimension and the zones overlap.
It is similar to m-trees, just not balanced.
There is no upper limit on the number of children.

It works for a general metric space.
Triangular inequality is assumed, as well as symmetry.
MetricTree deals well with non uniform clouds of points, that is, with clouds having zones with
high density of points along with zones where the points are spread at large distances.

MetricTree has been implemented with the intent of having wide usability.
It is templated over the type of points (the metric space) and over a callable
object returning the square of the distance between any two points.
However, it still needs the touch of someone experienced in the subtleties of C++.
Help is welcome.

An example of use is described in sections 12.10 and 12.11 of the
[manual of maniFEM](http://manifem.rd.ciencias.ulisboa.pt/manual-manifem.pdf).

Copyright 2020, 2021 Cristian Barbarosie cristian.barbarosie@gmail.com

MetricTree is free software: you can redistribute it and/or modify
it under the terms of the GNU Lesser General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

MetricTree is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Lesser General Public License for more details.

Full text of the GNU Lesser General Public License is available in files [COPYING](COPYING) and [COPYING.LESSER](COPYING.LESSER).
Or, see <https://www.gnu.org/licenses/>.
