# factory
Factory is an esoteric programming language that compiles into Javascript
<pre>

- Introduction to the factory:

In this language you control a claw in the byte factory, moving 1's and 0's around.
Here is a map of the factory on program start:
    |
    |
   / \
   \ /



    [1]    | _____________ | _____________ | _____________ |    X    |   [:=:]  | [    ] | !!!!!!!! | &&& 
production |storage space 1|storage space 2|storage space 3| garbage | shipping | supply | Invertor | and

The claw starts off over the leftmost room: production, where bits come in on a conveyer belt.

Here is the list of rooms, and how each behaves:

Production:
   This room will constantly be producing new bits, either 1s or 0s.
   When the factory starts, the production room will be producing 1s.
   These bits can be picked up by the claw and moved to where they need to go.
   If the claw places a bit in the production room, the room will switch to producing bits of that type.
   (i.e. if the claw places a 0, the room will start making 0s until the claw places a 1, and vice versa)
Storage spaces 1-3:
   These storage spaces start off empty.
   The storages can each hold one stack of bits.
   When a bit is picked up from storage, the one on top of all the rest is the one that is grabbed.
   When a bit is dropped off at storage, it is placed ion top of the stack.
Garbage:
   When a bit is placed in this room, it is destroyed, and cannot be recovered.
Shipping:
   This is where bits are loaded up to be sent to the Javascript alert box.
   When the factory is given a command to ship out, the bits in shipping will be grouped together into bytes of eight.
   These bytes are then each converted to 8-bit characters, and shipped as text.
   The message in binary is read from the bottom of the stack to the top.
   (i.e. if a bit is at the bottom of the stack, it will be the first bit of the first character)
   Placing and taking from this room is the same as in the storage rooms,
   but data stored here will be lost if the factory ships out.
Supply:
   The factory can ask for input from the javascript prompt box box.
   The input is recieved as text, and turned into the ascii binary for processing.
   When a shipment is recieved, everything in this room is moved to the garbage room to make space.
   The input binary is then placed here, with the message being bottom to top (opposite of shipping room)
   (i.e. if a bit is at the top of the stack, it will be the first bit of the first character)
   Placing and taking from this room is the same as in the storage rooms,
   but data stored here will be lost if the factory receives a shipment.
Invertor:
   This is one of the mighty machines in the factory.
   When a bit is placed in this room, it is changed into the opposite type of bit.
   After a bit is dropped off here, the new inverted bit can be picked up.
   WARNING: if there is a bit in the invertor, ready to be picked up, it will be destroyed if another one is put into the machine.
and:
   This is the factory's other machine.
   Bits can be picked up and set down om this machine, mach like in the memory rooms.
   However, if two bits are in this room at the same time the machine will turn on.
   When the machine turns on, it will check what kind of bits are in the room.
   If both bits are a zero, it will destroy one of them, leaving a 0.
   If one bit is 0 and one is a 1, it will destroy the one, leaving a 0.
   If both of the bits are 1s, it will destroy one of them, leaving a 1.

- basic commands:

The claw has very basic functions, as follows:

If the claw has the command BOOT
   it will turn on nd begin running each of the following command in order.
   the boot command must be on its own line
If the claw has the command <
   it will move left one room (unless it's in the leftmost room)
If the claw has the command >
   it will move right one room (unless it's in the rightmost room)
If the claw has the command v
   it will pick up a bit if it s not holding one
   or drop its bit off if it is holding one
If the claw has the command ^
   it will save the bit type to its one bit of RAM
   if it is not holding a bit, it will invert its RAM.
   Its RAM is set to 0 on bootup
If the claw has the command O
   it will ship the contents of the shipping room
If the claw has the command I
   it will ask for a shipment

- higher level commands:

The claw has four higher level commands: loop, eloop,and DEF, and q

DEF:
   def is run before the BOOT command, and defines a function.
   it is used by putting on its own line: DEF_
   followed by the name of the function.
   On the following lines, goes the functions code, which is run when the function is called.
   The end of the function comes when it finds the following keyword on its own line: END
q:
   If the claw finds this in a function, then the function will quit out, and the claw will go back to running its main code,
   even if the claw is running a loop
loop:
   If the claw's RAM is storing a 1, it will loop the code in the following {} brackets until the RAM is storing a 0 at the end of the brackets.
eloop:
   If this command follows the close of a loop, then the code inside the the following {} brackets will be looped until the RAM is stroring a 1 at the end of the brackets.

- extra notes:

To run a function, put the name of the function on its own line.

Anything between a / and the end of a line is a commet, and will be ignored.

Factory ignores spaces and tabs.
</pre>
<pre>
Example one: Hello, world!

/Hello, world!
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>>>vv<< v<<<<<
v>>>>>v<<<<<
O
</pre>
<pre>
-example two: I -> O program:
/IO program
DEF_checkHeld
   ^
   loop
   {
      ^
      loop
      {
         /holding 1
         q
      }
      eloop
      {
         /not holding
         q
      }
   }
   eloop
   {
      ^
      loop
      {
         /not holding
         ^q
      }
      eloop
      {
         /holding 0
         v^vq
      }
   }
END
BOOT
I>>>>>>v
checkHeld
loop
{
   <v>v
   checkHeld
}
O
</pre>
<pre>
- using Factory:
   the file named "factory.html" is the compiler.
   Up at the top are manual command buttons (the square is the RAM: red=0, green=1)
   The first text area is where the uncompiled factory code is to be written.
   "run code" compiles the code into Javascript and runs it.
   "compile code" compiles the code into Javascript without running.
   The text area below "compiled code" is where the Javascript version of the code is placed after being compiled.
</pre>
