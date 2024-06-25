# ML-Pathfinding-project-ECS-170
School project for ML


# A* Pathfinding Algorithm Implementations

This project provides multiple implementations of the A* pathfinding algorithm with different heuristics and strategies. These implementations are designed to explore various approaches to optimize pathfinding in grid-based maps. Each class extends the `AIModule` and overrides the `heuristic` and `createPath` methods to provide unique behaviors.

## Implementations

### 1. `AStarExp`

The `AStarExp` class uses an exponential heuristic based on the height difference between the current node and the goal node. This heuristic aims to prioritize paths with less elevation change.

#### Heuristic
```python
def heuristic(self, current, goal, map_):
    current_height = map_.getTile(current.x, current.y)
    goal_height = map_.getTile(goal.x, goal.y)
    y = goal_height - current_height
    x = max(abs(goal.x - current.x), abs(goal.y - current.y))
    if y < x:
        return x * math.exp(y / x)
    else:
        return y * math.exp(1 + (x - y))
