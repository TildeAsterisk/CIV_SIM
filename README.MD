#   CIV SIM
Agents and Nodes.

##  Nodes
Nodes are objects on the Grid that store information and other objects;
They tend to stay in their position.
Node Types:
- Resource
- Storage
- Home

##  Agents
Agents are objects that move around the grid according to a pattern of behaviour,
often moving between Nodes.
---

### **State Machine: Roaming Behavior**

#### **Roaming State**
**While in the Roaming State**  
- The agent **checks for enemies**:
    - If an enemy is detected, it will react accordingly (this behavior is not detailed here).
- If the agent has a **target**:
    - It moves toward the target.
    - While moving:
    - The agent **consumes resources** to stay active.  
        - If the agent **runs out of resources**, it:
        - Tries to locate a **resource node**:
            - If a resource node is found, it transitions to the **Gathering State**.
            - If no resource node is found, the agent **dies**.
    - Once the agent **reaches the target**, it selects a **new random position to roam to**.
- If the agent **does not have a target**, it selects a **new random position to roam to**.

##  Starting Progression
1. Begin with Home and Resource Node.
2. Gather Resources.
3. Build Storage Node
4. Updgrade Home to (Head Quarters, Hub, HQ, Citadel, Main Base, Central, Heart)
5. Defend against outdoor attacks
.. Further progression based on unit graphics, from tents to space...

---
##  To Do:
- [X] Update score to calculate total storage
- [ ] Implement Node team alliance flag. (Makes settlements easier.)
- [ ] Allow node to gather from a storage node.
- [ ] Graphics Updates
    - [ ] Different colour agents.
    - [ ] Build Menu with Icons
    - [ ] UI Rework
    - [ ] ASCII Graphics?
- [ ] Drain resource node that regenerates after cooldown
- [ ] Show Radius on selected Unit
- [ ] Develop Progression: Upgrades
- [-] Building Menu
- [ ] Nodes and Agents with behaviour states that consume resources from the storage nodes.
- [ ] Fix the weird checkForEnemy in State class implementation. Shouldnt be there...
- [X] Zero Player Game
- [X] Mulitple Agents
- [X] Combat

#   BUGS
- Fix questing. If one home is built, it completes all future quests of the same condition.
- After the game runs for a while there is a bug with the agentCapacity that crashes the game.

# Notes
Independant sections of CIVs with Resource, Storage and Homes are able to thrive competetively against eachother.


[Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)