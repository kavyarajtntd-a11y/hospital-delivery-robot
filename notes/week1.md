# Week 1 – ROS 2 Basics

## What is ROS 2?
ROS 2 (Robot Operating System 2) is a framework, not an operating
system. It runs on Ubuntu and provides tools and libraries for
building robot software as many small programs that work together.

## Nodes
A robot's software is split from one big program into smaller programs,
called nodes. Each node does one job.
For example, in turtlesim I ran two programs, turtlesim_node and
turtle_teleop_key. While running, their node names are /turtlesim and
/teleop_turtle.

## Topics
A topic is a channel between nodes.
For example, /turtle1/cmd_vel is the topic between /teleop_turtle and
/turtlesim.

## Messages
A message is the data sent on a topic. One node publishes messages on a
topic, and other nodes subscribe to that topic.
For example, each key press sends a Twist message with linear.x
(forward speed) and angular.z (turning speed).

## Services
A service is a one-off request and response.
For example, spawning a second turtle (turtle2) with the /spawn service.

## Actions
An action is for a long task, and it sends progress updates while it runs.
For example, the rotate keys (G, B, V...) turn the turtle to a set
direction and report progress until it is done.

## Commands I learned
- `ros2 run <package> <program>` – start a node
- `ros2 node list` – show running nodes
- `ros2 node info <node>` – details about one node
- `ros2 topic list` – show topics
- `ros2 topic info <topic>` – who publishes and subscribes to a topic

## Mistakes I made and what I learned
- Used `ros2 node info` on a topic name. Nodes and topics are different
  things, with different commands.