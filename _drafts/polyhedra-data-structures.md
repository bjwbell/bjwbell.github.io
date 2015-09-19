---
layout: post
title:  "Polyhedron Data Structures"
---

# Polyhedron

- Vertices: list of vertices
- Edges: list of tuples where each tuple is of the form (vertex index1, vertex index2)
- Faces: list of faces where each face is a list edge indices for that face
- Face adjacency matrix or list

# Wavefronts

- list of fronts

# Wavefront Node
A `wavefront node` is an enum of the below alternatives:

- ray: point (or possibly vertex index) + direction
- wide ray: point (or possibly vertex index) + (theta1, theta2). Where theta1 and theta2 are in the min and max angles with respect to the chosen axis.
- segment: (point1, angle1) + (point2, angle2) + edge index
