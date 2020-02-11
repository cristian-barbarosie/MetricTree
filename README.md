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

An example of use is described in sections 8.15 and 8.16 of the
[manual of maniFEM](https://webpages.ciencias.ulisboa.pt/~cabarbarosie/manifem/manual-manifem.pdf).

Copyright 2020 Cristian Barbarosie cristian.barbarosie@gmail.com

MetricTree is free software: you can redistribute it and/or modify
it under the terms of the GNU Lesser General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

MetricTree is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Lesser General Public License for more details.

You should have received a copy of the GNU Lesser General Public License
along with MetricTree.  If not, see <https://www.gnu.org/licenses/>.
