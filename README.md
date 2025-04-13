Use WASD to move your character and left click to shoot. Each Hero has a pool component of several missiles. When the player presses the left click button it shoots a missile on the server (max 1 missile each 0.125 sec).
The server replicates the initial position, the yaw and the speed of the missile on all clients, there is also a RepNotity byte "Trigger" variable that increases each time the player shoots. That "Trigger" variable then triggers the move of the missiles on the client side according to the replicated variables.
However with lag it can happen that the missile is not exactly on the same position on the server and on the client, or the RepNotify can even not trigger.

I would like that no matter what (lag) clients always see the missile at the correct server position.

Things to know :
- All players should have the missiles trajectory because in the actual game no matter the player posision, the player is able to teleport anywhere on the map and they would need to see the missiles if he teleports somewhere near some of them.
- If the client has 100 ms and there is a 100ms delay between the click (to launch a missile) and the actual spawning of a missile on the server, that is not a problem, I DO NOT want lag compensation for that.

Here the client on the left should see the missiles (the white cubes) at the same location as the server :

![test](https://i.ibb.co/ccQTV8T7/Capture-d-cran-2025-03-23-144120.png)
