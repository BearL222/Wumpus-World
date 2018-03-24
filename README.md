# Wumpus-World
## Algorithm
AI saves the explored rooms in the path set and the unexplored safe rooms in the children set.


AI considers all rooms in children set as goals and uses BFS search algorithm to find a room as target. Then A* search algorithm is implemented to generate optimal action sequence. AI will terminate and exit when gold has been grabbed or there is no room in the children set.


After reaching a goal room, AI will add current room to the path set and remove it from children set. If there is no breeze and stench perceived, AI adds the adjacent rooms to the children set. If stench is perceived, AI marks all rooms except the adjacent room as non-Wumpus (Initially all rooms are marked as Wumpus in the AI recorded map). 


According to the cost of all goals calculated by A* algorithm, AI implements UCS algorithm to find a goal and generate optimal action sequence.


If the stench is perceived and there is only one Wumpus mark in the recorded map, generating action sequence to shoot the Wumpus.
