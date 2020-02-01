# MetricTree

MetricTree is a tiny C++ library for organizing hierarchically a cloud of points in 
an arbitrary metric space.
It is similar to quad- and oct-trees with two differences :
there is no assumption on the geometric dimension and the zones overlap.
It is similar to m-trees, just not balanced.

It works for a general metric space.
Triangular inequality is assumed, as well as symmetry.
MetricTree deals well with non uniform clouds of points, that is, with clouds having zones with
high density of points along with zones where the points are spread at large distances.

There is no upper limit on the number of children.
Actually, the average number of children can be used as an hint about the dimension of the
metric space (in the spirit of Hausdorff dimension).

MetricTree has been implemented with the intent of having wide usability.
It is templated over the type of {\codett Point}s (the metric space) and over a callable
object returning the square of the distance between any two {\codett Point}s.
However, it needs the touch of someone experienced in the subtleties of {\codett C++}
to become a widely usable library in the style of {\codett STL}.
Help is welcome.

An example of use is described in sections 8.15 and 8.16 of the
[manual of maniFEM](https://webpages.ciencias.ulisboa.pt/~cabarbarosie/manifem/manual-manifem.pdf).

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Lesser General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Lesser General Public License for more details.

You should have received a copy of the GNU Lesser General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
