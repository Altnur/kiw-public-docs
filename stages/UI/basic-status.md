# Basic Status

The UI for basic status should show:

- HP
- MP
- Level
- Experience

## Position

Like many RPGs I want the basic ui status bars needs to be in the upper left corner of the screen.

Maybe it will be possible to arrange it, along with other ui elements, I don't know it yet.

## Minimalism behavior

I want to show the info the moment the player needs it.

For example, showing the HP only when the player has been hit, and the current HP is lower than the max HP.

With that in mind, the rest would follow like this:

- MP: When the current MP is lower than the max HP
- Level: When the player level up.
- Experience: When the player get experience.

This behavior is toggleable with a little button, next to the status bars.

## Dependences

This stage depends on:

- [Basic Attributes](../basic-attributes.md)
- [Level and Skills System](../basic-attributes.md)