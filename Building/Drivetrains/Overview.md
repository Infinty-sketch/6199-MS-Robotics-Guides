# Overview
> [!NOTE]
> No decision you make should be made at random, everything needs to have a reason.

You need to go into building with a plan, this can be a CAD, or simply a detailed drawing.
> [!WARNING]
> **A PLAN THAT IS IN SOMEONE’S HEAD IS NOT A GOOD PLAN!**

Going in without a well build plan results in a incomplete build and oversights that would have been voided; in all, no plans = jankiness

In terms of drive trains, they obviously need to move the robot around, but what does it need to do in order to function with the rest of your robot? You need to take into account the rest of the robot. If you had a weight distribution problem, you might want a long drive base to prevent tipping, if you want large subsystems in the front/back of the robot, you might want to have a shorter drive base to leave room for this. In this year’s game (2023/24) you must also have to be short and narrow enough to easily move between sides so that would also be taken into consideration.

> [!TIP]
> **TLDR: Use CAD software.**

### Size:
Make sure to take into consideration how much space you will need for future mechanisms on the robot. This should not be chosen at random, the number of wheels, the size of obstacles on the field, and any size constraints that the game forces on the Robot should all be taken into account.
### C Channels (Materials):
I hope this is obvious but c channels should be the only thing used on a drivetrain (PLEASE DO NOT USE STEEL) Sizewise there are 3 types of c-channels, with them being 2, 3, and 5 holes wide. 2 wide C-Channels (left) is most commonly used, and 3 wide (middle are sometimes used to better mount something. 5 wide is so big it’s almost never used.

<img width="485" alt="Screenshot 2024-01-24 at 7 47 59 PM" src="https://github.com/Arcx23/6199-MS-Robotics-Guide/assets/132633896/66702581-8ffe-49e8-93c7-7dfd4b25df25">

### Motors, Wheel Size, and Gear Ratio (Materials+Detailed):
Refer to [Calculations](https://github.com/Arcx23/6199-MS-Robotics-Guide/blob/main/Building/Drivetrains/Overview.md#calculations): after reading

Motors should not be picked at random. For drive trains, only blue or green motors    can be used, and pretend red motors do not exist. Green motors rotate slower, but exert significantly more torque and blue motors spin much faster but the trade off is that they exert much less torque and often burn out very quickly. 

Wheel size is a pretty simple decision, you have between 4", 3.25", and 2.75" wheels. You should almost always be using Omni Wheels, flex wheels to lock the base in place works, but is not always a necessity for every year’s game.
Smaller wheels make your robot slower, but have a lower center of gravity and distributes the weight evenly across the tiles → less sinking in tiles. For example, smaller wheels would be slower, but they could be more stable and they have a smaller gap in between wheels so they might not get stuck on objects as much. However, a set of larger wheels would be faster, but at the cost that the Robot tips over much easier and you can fit fewer wheels per side. At the other end, smaller wheels provide a much more stable base, but results in a slower robot 

Gear ratio is a much more complicated decision, you first need to be aware of what kind of speed you’re after.
In games that involve lots of small, short movements, and heavy robots, teams might choose a ratio around 200 rpm on 4" might be a good idea, for high torque and good acceleration. For a game where robots weigh very little, and need to zip around at high speeds, rpms from 300 to even 400 on 4" wheels might be more suitable.

>[!TIP]
>**TLDR: High Speed = Less Torque; Low Speed = High Torque.**

### Drivetrain Bracing:
Your drive needs to have proper bracing so that it stays rigid and cannot flex or deform. At a minimum you should have two cross braces between the two sides of your drive. The further apart these braces are, the more robust the drive will be. It's also a good idea to brace these braces..

One way of doing this is to create one primary brace, usually at the very back of the drive, and make it as strong as possible. This means multiple c channels, standoffs, box bolts, (explained later) everything to keep this brace as strong as possible.

Then you can add a secondary brace typically closer to the front of the robot either on the bottom or top depending on other design choices.
Another good thing to do is to brace the channels that house the wheels. This can be done with standoffs, small cchannel, etc.

<img width="215" alt="Screenshot 2024-01-24 at 7 48 25 PM" src="https://github.com/Arcx23/6199-MS-Robotics-Guide/assets/132633896/4e71e831-b2e1-4eae-a5ff-523f066819c8">

> [!IMPORTANT]
> Seen above is a Cad of a robot displaying proper drivetrain bracing.

### Calculations: 
Let's say you want to know how fast your wheel will turn with x gear ratio, and motor speed. 
[Calculator](https://www.omnicalculator.com/physics/gear-ratio)
4 inch wheel
200 rpm motor
60:36 gear ratio (input gear = 60 teeth, output gear  = 36 teeth)
Provides an output rotational speed of 375 rpm
375 rpm/60 seconds = 6.25 rotations per second
6.25 rotations * 4 inches/1 second = 25 inches/second (Assuming No Friction)

### Box Bolting:
Box bolting is where you fill the gap between a c channel’s flanges with spacers or standoffs, so that it becomes almost impossible for the flanges to bend.

>[!IMPORTANT]
>This should be utilized whenever you connect your c channels (unless otherwise impossible)

Here is what it looks like to use box bolts:

<img width="241" alt="Screenshot 2024-01-24 at 7 52 09 PM" src="https://github.com/Arcx23/6199-MS-Robotics-Guide/assets/132633896/857df228-6100-4e1e-8a22-13a863cc408f">

### Power:
The way power is handled in drives is up to you. Common methods of power 
and transferring it are as follows. Chains, direct motor linkage, and gears

Chain is generally frowned upon when it comes to drives. The reason for this is that it snaps. For most teams, this is an unacceptable risk to take on the most essential system, Unless both wheels are connected directly to a motor. So when the chain breaks, both wheels keep moving and the drive can continue to operate almost as normal. 

Directly mounting your wheels to motors is also an effective and simple way to power your drivetrain although it is recommended that you also chain together the wheels for synchrony between wheels and power transfer if one wheel loses contact.

The _Best_ way to power your drivetrain is with gears. Gears give you utmost control of torque and speed while also being extremely consistent in keeping power to all wheels. I would recommend every team to use gears on their drivetrain. 

### Joints:
Typically your drivetrain should have 4,6 or 8 joints depending on how many wheels you have. The spacing on these joints is pretty forgiving as far as tolerances go.

- ### Consider This:
  - chain/gears and the wheel should not scrape against side c channels
  - spacing should not be too tight → creates unnecessary friction
  - A good rule of thumb with joint spacing is that you should leave a gap big enough to stick your fingernail in
  avoid any metal-on-metal rubbing, which means that shaft collars shouldn’t be touching any c channels directly
  - Separate shaft collars from metal with at least a washer
    
Another important part of the joint is that both the sprocket and wheel need to be locked to the rotation of the shaft, using square inserts. This way the motor is able to transfer its rotational motion through the shaft into the wheel and sprocket. Try to avoid using old omni wheels or sprockets that have plastic square inserts because those tend to wear out and let the sprocket or wheel wiggle against the shaft. 

Another hugely important part of joints is what the joint is spinning on. In many cases, including this one, that thing is a bearing flat. Bearing flats provide a smooth, round hole for the shaft to spin in. Without the bearing, the square shaft will be pressed and ground against the square hole, which will eat away at the metal and create huge amounts of friction. The shaft should never come into contact with the c channels at any point.

### end
