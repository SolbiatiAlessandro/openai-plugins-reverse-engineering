The CreatiCode plugin is an extension for MIT Scratch, a block-based visual programming language. This plugin allows ChatGPT to display Scratch programs as images instead of pseudocode, making them easier to read. It also provides the syntax and function of new blocks created by CreatiCode.

The namespace `Creaticode_Extension_of_MIT_Scratch` contains the following type definitions:

1. `getCodeImageForOnlyOneStack`: This type is used to get the image representation of a single stack of blocks. It also provides additional explanations about the programs. The fields for this type are:
   - `spriteName`: A string representing the name of the sprite.
   - `pseudocode`: A string containing the pseudocode of one stack of code for one sprite. All blocks should conform to the syntax returned from the 'getBlockDescription' API. For programs with more than one sprite, or sprites with multiple stacks of blocks, this API should be called multiple times for each stack in each sprite. A stack of blocks is a sequence of blocks that are connected together. It should start with a hat block like 'when green flag clicked' or a 'define' block for custom block definition.
   - `userPrompt`: A string containing the original user prompt.

2. `getAdditionalBlocksInfo`: This type is used to get the IDs of additional new blocks. The fields for this type are:
   - `projectType`: A string that specifies the type of project. It can be '2DOnly' for 2D-related blocks or '2D3D' for all new blocks.

3. `getBlockDescription`: This type is used to get the syntax and function of the blocks based on their IDs. The fields for this type are:
   - `blockIDs`: A list of strings representing the IDs of the blocks.

4. `getCodeImage`: This type is used to convert the pseudocode to images. When the program has multiple sprites, it generates one image per sprite. The fields for this type are:
   - `pseudocode`: A string containing the pseudocode of the code for the sprites. All blocks should conform to the syntax returned from the 'getBlockDescription' API.
   - `userPrompt`: A string containing the original user prompt.

These types provide a way to interact with the CreatiCode plugin, allowing the user to generate images of Scratch programs, get information about additional blocks, and understand the syntax and function of these blocks.
