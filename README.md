# pokeemerald Expansion

## What is the pokeemerald Expansion?

The Pokeemerald Expansion is a collection of feature branches that can be integrated into existing [pokeemerald](https://github.com/pret/pokeemerald) projects.

## What is this branch?

This feature branch contains a dynamic npc system. These dynamic NPC's are stored in the saveblock, and will persist exactly where you left them for as long as you want them to be there. This is good for spawning an object at a remote location for, say, a quest, and not having to deal with messy map scripts or waste flags on hiding/showing one time use objects. 

### IMPORTANT INFORMATION
Merge Difficulty: Intermediate (7/10)
 You may have to free up space for this feature branch in your save block
 This may interfere with follower systems that use localid's 0xF0 thru 0xF3.

#### Usage Difficulty: Intermediate (5/10)
 This branch modifies the overworld object spawn function, performance can suffer.
 This branch offers minimal error checking and assumes you know what you are doing.

#### Requirements: 80 bytes of free space in SaveBlock1. 
 (This branch reduces the number of secret bases from 20 to 18 in order to free up 320 bytes of space in SaveBlock1.)
 Note that at the default dynamic object count, the lag is minimal, Adding more dynamic object slots will also increase lag when there are dynamic objects active in the overworld. This could potentiall by optimized out, but that is up to the end user.

### How to use
There is an example script posted on the Littleroot Town sign. It shows everything necessary to use the system.

## FAQ
Q: Will this interfere with my followers (if you have them)?
A: The dynamic objects use overworld objectIDs F0 thru F3. If your followers are using these id's then, yes they will interfere.

Q: Do I need the dynamic overworld palettes or overworld expansion system to use this?
A: Probably not, but spawning dynamic objects that use palette slots reserved by other objects may result in corrupted palettes. This feature branch does not modify or use any special graphics or palettes. You supply an existing obj_gfx_id




## What features are included?
- Upgraded battle engine.
    - Fairy Type.
    - Physical/Special/Status Category Split.
    - New moves and abilities up to SwSh.
    - Options to change behaviors and data by generation.
    - Mega Evolution and Primal Reversion
    - Z-Moves
- Pokémon Species from newer Generations (with the option to disable them if needed).
    - Updates Hoenn's Regional Dex to match ORAS'.
    - Updates National Dex incorporating all the new species.
    - Option to change base stats by generation.
    - New evolution methods.
    - Hidden Abilities data (How to make them available is up to the user).
- Items from newer Generations and updated item effects for battle and field use.

Certain mechanics, moves, abilities and species sprites are missing. For more information, see [the project's milestones](https://github.com/rh-hideout/pokeemerald-expansion/milestones).

### [Documentation on features can be found here](https://github.com/rh-hideout/pokeemerald-expansion/wiki)

## Who maintains the project?

The project was originally started by DizzyEgg alongside other contributors.

The project has now gotten larger and DizzyEgg is now maintaining the project as part of the ROM Hacking Hideout community. Some members of this community are taking on larger roles to help maintain the project.

### Please consider crediting the entire [list of contributors](https://github.com/rh-hideout/pokeemerald-expansion/wiki/Credits) in your project, as they have all worked hard to develop this project :)

## Can I contribute even if I'm not a member of ROM Hacking Hideout?

Yes! Contributions are welcome via Pull Requests and they will be reviewed by maintainers. Don't feel discouraged if we take a bit to review your PR, we'll get to it.

## What is ROM Hacking Hideout?

A Discord-based ROM hacking community that has many members who hack using the disassembly and decompilation projects for Pokémon. Quite a few contributors to the original feature branches by DizzyEgg were members of ROM Hacking Hideout. You can call it RHH for short!

[Click here to join the RHH Discord Server!](https://discord.gg/6CzjAG6GZk)
