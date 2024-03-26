## Euclidean distance
Euclidean distance, named after the ancient Greek mathematician Euclid, is the straight-line distance between two points in Euclidean space. It is the most common use of distance in geometry, representing the shortest way to travel between two points.  

```
import math

def euclidean_distance_nd(point1, point2):
    return math.sqrt(sum((p1 - p2) ** 2 for p1, p2 in zip(point1, point2)))

# 例子
point1 = (1, 2, 3)
point2 = (4, 5, 6)
distance = euclidean_distance_nd(point1, point2)
print("The Euclidean distance between the two points in N dimensions is:", distance)
```
