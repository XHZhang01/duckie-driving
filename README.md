## Usage

This project is aimed at autonomous driving of Duckiebots in a mini city. It has four components, namely lane following, odometry, intersection navigation and state machine.

1. Lane following
It detects the white line and the yellow line from the camera images. The Duckiebot can follow and lane and stay in the middle.

2. Odometry
It localizes the Duckiebot with dead reckoning and gives its coordinates in global map. Every time the Duckiebot stops at the red line, this odometry is reset to reduce the accumulated drift.

3. Intersection navigation
It guides the Duckiebot through the intersection. It first detects the red line at the intersection and forces the Duckiebot to stop. Then right turn and left turn are realized by path planning with waypoints and PID controller.

4. State machine
It demostrates the current state of the Duckiebot by different light colours and lets the Duckiebot switch among different modes, namely still, forward, backward, right turn and left turn.

## Execution
1.Build docker image on duckiebot

Run command

`dts devel build -f -H <robot_name>.local`

Replace `<robot_name>` with name of your duckiebot.

2.Start docker container

Run command

`dts devel run -H <robot_name>.local`

Replace `<robot_name>` with name of your duckiebot.

