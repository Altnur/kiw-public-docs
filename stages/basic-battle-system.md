# Basic combat system

The key of every rpg game, the combat system.

I need to include multiple things on this:

- First, the items, we have 2 types:
    - Melee weapons
    - Range weapons

All of them, children of a base item called Weapon.

## Weapon

All weapon have:

- Damage: The damage that it inflicts.
- Preparation: The time until the weapon attacks
- Cooldown: The time until the weapon can attack again
- CharacterAnimation: The name of the animation that the player will play when it attacks
- WeaponAnimation: The name of the animation that the weapon will play when it attacks

When the item Weapon is used, a clock will run, until the clock reach Preparation time, and then a custom function will be called, and this function is the function that will be in our children objects.

## Melee weapons

They should instantiate a hitbox, with the length of the weapon, for a few moments, in the front of the player.

The hitbox should be customizable, to allow, for example, daggers and longswords, or even spears that cover a wide range.

The melee weapon have:

- Hitbox position (x and y)
- Hitbox size (width and height)

## Range weapons

These weapons shots a projectile, they dont inflict damage directly, but thanks to the projectile they launch.

Their damage is the combination of the projectile + base damage of the weapon.

Range weapons have:

- Projectile type (Arrows, bolts)
- Range

## Projectile

The item projectile is just an auxiliar item for the ranged weapons. They are stackable, and have a type associated

Projectiles have:

- Type

## Damage

The, I need to actually inflict, damage, for that, if the collision triggers on something, and that something is a character, the OnHit event should be called.

## Dependences

This stage depends on:

- [Stackable items](./stackable-items.md)
- [Stackable items](./equipable-items.md)
- [Basic constitution](./basic-constitution.md)
- [Basic attributes](./basic-attributes.md)