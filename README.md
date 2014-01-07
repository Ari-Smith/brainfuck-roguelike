brainfuck-roguelike (working title)
-----------------------------------

A simple roguelike written entirely in brainfuck. So far the project is very promising but it is still a long way to go.

Here are some notes on the mechanics and how to play:

    - Because some brainfuck interpreters or compilers only allow input to be added in the very beginning, it is currently 
    working in a way such that, in the very beginning you must input a "save state code", followed by a space, and then 
    your desired move. The program will then output an ASCII map of the game, and then a new code to reinsert in the next 
    time you run the program, which would be the player's next turn. I will eventually create a continuous version of the 
    game for interpreters that allow input later on, which will not have any confusing codes or things like that.
    - A save state code will look very much like line noise. It is structured as such:
    
        - The x dimension of the room (not including walls), plus 33, then represented as an ASCII character
        - An exclamation point ("!")
        - The y dimension of the room, modified as described above
        - Four exclamation points
        - The player's x coordinate, modified as above
        - The player's y coordinate, modified as above
        - The letter "a"
        - The x coordinate of any object/obstruction, modified as above
        - Its y coordinate, modified as above
        - The lower-case letter AFTER the capital letter you desire for the object to be represented by on the screen
        - Repeat the last three steps as many times as you want for as many objects as desired
        - Example: +!+!!!!'&a(&b)'c)(d()e')f&(g&'h
        
    - So far, the game consists of a player moving around a rectangular room of any size, with non moving obstructions. 
    Obstructions will eventually become enemies, items, doors and obstructions as they are now.
    - Finally, I cannot seem to find any sort of standardized file type, so I have left it as a .txt file for you to 
    figure out what to do with it.
