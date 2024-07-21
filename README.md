# Valorant-Best-Crosshair-Color
- Determines the best crosshair color when playing the 3D tactical shooter game Valorant

## Steps Performed
1. Obtain the textures of each Valorant agent by following this [guide](https://www.reddit.com/r/VALORANT/comments/qf16q8/guide_to_viewingextracting_3d_valorant_models_of/) from Reddit
2. With umodel application opened, navigate to the Characters->"A Particular Agent Folder"->S0->3P->Models->"One of the uasset files"
3. Screenshot the texture files for use in the Python code and repeat step 2 for other Valorant agents
4. Determine the average RGB color of texture files for each Valorant agent and find the average color
5. The best crosshair color is then determined by finding the complementary color of the average color found from the previous step
   - use of complementary color as the acclaimed best crosshair color is based on color theory where complementary colors have high contrast and stand out more vividly

## Thought Process and Considerations
- "Best" Crosshair color is affected by:                                                                              Remarks
   1. Color of the map                                                                                               (Possible but time consuming)
   2. Color of Enemy outline                                                                                         (Aim is to contrast the enemy color instead of the enemy outline color)
   3. Color of abilities                                                                                             (Too conditional)
   4. Color of Enemy in certain states: When Enemy Blinded/Stunned/in Viper Ultimate, Reyna Activated Ultimate, etc. (Too conditional)
   5. Color of Enemy gun                                                                                             (Overkill for this project)
   6. Color of Enemy gun buddy                                                                                       (Overkill for this project)

## Areas of Improvement worth exploring
1. Incomplete Valorant Agent Texture:
   - The above texture files are only of the body of the Valorant Agents.
   - The texture of the eyes and hair of the Valorant Agents are in different texture files and are not to scale
   - Possible solution: Try to scale texture files of hair and eyes based on the size of the head in the body texture file  
2. Crosshair color affected by color of map
   - Possible solution: Capture enough screenshots of each map and use it to determine the average color of the map and then combine with the average color from the steps above before finding the complementary color
   - The same above steps cannot be performed on map textures as they are all coloured red and black
3. Instead of performing the above steps for all Valorant Agents, they should only be performed on the five agents picked by the opponent in each game
   - Possible Solution: Using the average colors already found from the Python file, find the complementary color for every possible combination of 5 Valorant Agents picked by the opponent

  
