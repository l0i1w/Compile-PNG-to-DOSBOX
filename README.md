-- SPRITE SHEET --
1) Must be .png format
2) All sprites must be same width and height

-- HOW TO USE DOSBOX TURBO C++ CONVERTATION --
1) Put your sprite sheet into folder "Sprites"
2) Open file "Convert.py" and enter:
 2.1) Sprites in a row
 2.2) Sprites in a column
 2.3) Width of one sprite
 2.4) Height of one sprite
3) After convertation open file "SprTextToClass.py" and enter:
 3.1) Class name
 3.2) How much spaces (tabs) you need
4) You will get inside "Classes" folder your class
5) Copy that class and paste it into include folder (in turbo c++ include folder)
6) You can get example of png reader in "CPPReader" folder
7) Pick example with or without including "graphics.h"

-- HOW TO PUT SPRITE IN PROGRAM (WITHOUT GRAPHICS.H) (RECOMMENDED) --
1) Inside your program include <wtool.h>
 1.1) Also include your class with sprites
2) Inside main function do:
 2.1) Create new class "WinTools" (lets call it w)
 2.2) Create new class "classwithyourspritesname" (lets call it s)
 2.3) Assign values for window with:
  w.Assign(width,height,bgcolor)
  bgcolor is from 0 to 15
 2.4) After making class refresh window with:
  w.Refresh()
 2.5) Now, to make sprite use:
  w.ReadTxt(s.spr1,width of sprite, height of sprite, position x, position y, scale x, scale y)
  Instead of s.spr1 use s.spr with index of your sprite
  Width and height of sprite is full width and full height
 2.6) To show screen, use:
  w.Show(position x, position y, scale x, scale y, show full screen)
  Where show full screen 1 if you want full screen, 0 if not
 2.7) Finally, like in every function, return 0
3) Try to run it
If you want, you can open my example in folder "CPPReader"

-- HOW TO PUT SPRITE IN PROGRAM (WITH GRAPHICS.H) (NOT RECOMMENDED) --
1) Include <wtool.h>
 1.1) Also include your class with sprites
2) Inside your main function do:
 2.1) Create new class "Wintools" (lets call it w)
 2.2) Create new class "classwithyourspritesname" (lets call it s)
 2.3) Import graphics with:
  2.3.1) int gd=DETECT,gm;
  2.3.2) initgraph(&gd,&gm,"C:\\BGI");
  2.3.3) in the end inside function main do: closegraph();
 2.4) To clear screen use cleardevice();
 2.5) Now, to make sprite use:
  w.ReadTxt(s.spr1,width of sprite, height of sprite, position x, position y, scale x, scale y)
  Instead of s.spr1 use s.spr with index of your sprite
  Width and height of sprite is full width and full height
 2.6) Finally, like in every function, return 0
3) Try to run it
If you want, you can open my example in folder "CPPReader"
