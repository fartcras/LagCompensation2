Use WASD to move your character and left click to shoot. Each Hero has a pool component of several missiles. When the player presses the left click button it spawns a missile on the server. The server replicates the initial position, the yaw and the speed of the missile on all clients. Then the clients move themselves the missile according to those replicated variables. However with lag it can happen that the missile is not exactly on the same position on the server and on the client.

I would like to synchronize the position of the client's missile with the position of the missile on the server once the missile has been spawned. So clients see the missile at the correct server position.

Just to precise : if the client has 100 ms and there is a 100ms delay between the click (to launch a missile) and the actual spawning of a missile on the server, that is not a problem, I DO NOT want compensation for that.

![test](https://i.ibb.co/ccQTV8T7/Capture-d-cran-2025-03-23-144120.png)
