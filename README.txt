Author - Toni Vuoristo, Greatshader@hotmail.com
Icons  - Väinö Savolainen, vaino.savolainen@skill-arena.com

current version 1.13

NEW Webcamera support for reading colors using webcamera
    takes the images on same pattern as applying the sides
    through manual adding (Top->Front->Down->Back->Right->Left)
    ver 1.13

NEW Iterative searching !
    allows searching of the solution from deeper
    ver 1.21!
    
contains the following exe(s):
    TRubik.exe
    TRubik3D.exe()
    w9xpopen.exe(Ignore this!)

TRubik is a 3x3 rubiks cube solver. the solver relies on Fridich method to solve the cube.

key features:
    *can be invoked through cmd with - cd *path to TRubik folder* & start TRubik.exe 'colors.txt'
    if the folder is on say.. desktop i would use: "cd desktop\TRubik & start TRubik.exe Array3D.txt"
    which would start the TRubik and read the Array3D.txt and output immediately the solve for it
    if ofcourse its solvable..
    
    *contains settings to control the program(more settings will be released future updates)

    *includes a 3D display with speed control(Arrow keys to control the speed. 1 = fastest)
    also can be invoked through with cmd be careful tho the TRubik3D.exe takes 2 extra cmd line arguments
    - First one is preserved for the solvemoves 
    - second one is for the colorarrays 
    BOTH are needed!
    
    the ColorArray.txt is always created on this same style:
    face the side based on this table
        -Top(Red on top)
        -Front(White on top)
        -Down(Orange on top)
        -Back(White on top)
        -Right(White on top)
        -Left(White on top)
        * Color keys to identify the sub-cube side
        -White  = 1
        -Orange = 2
        -Yellow = 3
        -Red    = 4
        -Green  = 5
        -Blue   = 6
    
    when facing the side add the colors from TopLeft to DownRight
    eg. if im facing the top(white by default) the red-side would be the top now
     
   (Red on top)
    1 | 1 | 2
    ---------
    3 | 1 | 5  <--- example White face
    ---------
    5 | 6 | 4
    
    i would add the following numbers to the first line 11235564(we can ignore the middle since it always stays the same)
    now you can add the rest based on the tables above. Every side goes on its own line(This is important!)
    the reader is very strict with the reading of this given file so double make sure that its correct!
    also remember to add the sides on that above side order. Once the file is created, we can throw it for the solver
    and it'll output the solve.txt for it

    the solver isn't perfect however and its not even close to god number 20 solving the whitecross sometimes may
    take more moves than needed