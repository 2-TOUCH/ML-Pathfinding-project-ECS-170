# ML-Pathfinding-project-ECS-170
School project for ML

# A* Pathfinding Algorithm Implementations

This project is a school assignment designed to highlight different implementations of the A* pathfinding algorithm. It explores various heuristics and strategies to optimize pathfinding in grid-based maps.

## Implementations

Each implementation extends the `AIModule` and provides unique behaviors by overriding the `heuristic` and `createPath` methods. These variations demonstrate how different approaches can impact the efficiency and effectiveness of the pathfinding process.

## How to Use

1. **Clone the Repository**:
    ```sh
    git clone https://github.com/your-repo/astar-pathfinding.git
    cd astar-pathfinding
    ```

2. **Install Dependencies**:
    Ensure you have Python installed. You may need to install additional libraries, which can be done via pip:
    ```sh
    pip install -r requirements.txt
    ```

3. **Run the Algorithm**:
    Example script to run an implementation:
    ```python
    from astar import AStarExp
    from map import Map  # Assuming you have a Map class implemented

    map_ = Map('path/to/mapfile')
    start = map_.getStart()
    goal = map_.getGoal()

    astar = AStarExp()
    path = astar.createPath(map_, start, goal)

    print("Path found:", path)
    ```
