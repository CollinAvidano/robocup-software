
# Path Planning

Path planning is one of the most vital subsystems of the Robocup software stack. It forms the bridge between the low level systems of motion control, which control 
motors directly, assuring that we are moving accurately along a path, and the game
play module, which abstracts away these systems to a move command with a target point. 
Soccer does not have one uniform path planner. But instead many different planners that have consistent outputs and dependencies. This allows us to have different behavior for finding paths.

Soccer defines all classes relevant to path planning under soccer/planning. 
RRT(Rapidly exploring Random Trees) is the general purpose path planner employed by the team. The RRT planner generates tree nodes outwardly from both the starting 
point and the target position linking the two trees when they are. The nodes stop going in a direction when they hit an obstacle.  For most purposes, The RRT planner should be a sufficient path planner. 
