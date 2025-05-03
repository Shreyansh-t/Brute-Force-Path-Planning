Hardware Setup & Calibration

Mount the Intel RealSense camera on the robot and calibrate its depth intrinsics.

Verify real-time streaming of 3D point clouds into your processing pipeline.

Point-Cloud Preprocessing

Apply voxel down-sampling to reduce noise and density.

Project the filtered 3D cloud onto a 2D occupancy grid (choose resolution to balance detail vs. speed).

Planner Implementation

Integrate A*, RRT, and RRT* algorithms within the same framework so they share the same map and start/goal interfaces.

Ensure RRT* supports incremental rewiring and that all planners can return both path and timing data.

Define Evaluation Metrics

Path Quality: total length and clearance margin

Compute Performance: planning time and memory usage

Robustness: success rate in narrow passages and dynamic replans

Static‐Map Experiments

Select 10 representative start–goal pairs covering open areas and tight corridors.

Run each planner 30 times per pair, logging path, time, and clearance.

Dynamic Obstacle Trials

Introduce moving obstacles during execution and trigger replanning.

Measure replanning latency and success under obstacle perturbations.

Data Logging & Analysis

Store all trajectories, timestamps, and metric values in CSV or a database.

Use scripts to compute averages, standard deviations, and to plot comparative charts.

On-Robot Validation

Replay the best trajectories on the physical robot in the obstacle course.

Confirm real-world tracking accuracy and end-to-end latency, ensuring ≥90 % safety compliance.
