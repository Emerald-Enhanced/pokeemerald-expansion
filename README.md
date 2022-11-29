## Dynamic Multichoices

This is a feature branch that makes script multichoices (pory and standard!) much more sane to use and edit. Never have to add a whole multichoice menu to 4 different files again!

It's pretty simple to use.

First step is to 
bufferdynamicmulti string1, string2, string3, . . . (up to 6 strings can be specified. Missing strings will be filled automatically.)
then 
multichoice Xloc Yloc, MULTI_DYNAMIC_Z, ignoreB where Z is the number of choices you want your menu to have.
Other than this, it works exactly like the standard multichoice. This allows you to generate multichoices in your script rather than having to define new constants in other files for them.
Example Porycript:

text MNM_1 {
    "Sweet"
}

text MNM_2 {
    "Spicy"
}

text MNM_3 {
    "Sour"
}

script myNewMultiScript {
    msgbox("What's your favorite flavor?")
    bufferdynamicmulti(MNM_1, MNM_2, MNM_3)
    multichoice(0, 0, MULTI_DYNAMIC_3, 1)
    switch (var(VAR_RESULT)) {
        case 0:
            msgbox("You chose Sweet!)
            goto(sweetScriptActions)
        case 1:
            msgbox("You chose Spicy!)
            goto(sweetScriptActions)
        case 2:
            msgbox("You chose Sour!)
            goto(sweetScriptActions)
    }
    release
    end
}

And this is all you need! No more tracking multiple files for basic multichoices!

# NOTICE FOR MERGING!
### BEFORE merging this, to save yourself a headache, replace EVERY INSTANCE of "gStringVar4" with "gSystemStringVar"
### There should be NEAR 800 INSTANCES.

==ORIGINAL README BELOW==

# What is the pokeemerald Expansion?

The Pokeemerald Expansion is a collection of feature branches that can be integrated into existing [pokeemerald](https://github.com/pret/pokeemerald) projects.

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
