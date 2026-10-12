# Job and weapon overrides

**Tag:** `JOB_WEAPON_OVERRIDES`

**Created In:** https://github.com/Shadow-Fragger-Metaclique-Gang/TheImpossibleDream/pull/40

**Major changes:**

## Ducal standards

Ports [Ratwood PR #3017](https://github.com/Rotwood-Vale/Ratwood-2.0/pull/3017) (Yuckuza)

- `code/ducal_standard.dm`: pike intents, a poleaxe with three grip movesets,
  weapon special selection, strapless, and two-tone ducal scheme banner colors.
- `code/standard_bearer.dm`: removes the greatweapon strap, assigns the standard
  choices
- `icons/ducal_standards.dmi`: upstream standard sprites

## Drow merc reflavor and expansion

Ports [Ratwood PR #2589](https://github.com/Rotwood-Vale/Ratwood-2.0/pull/2589) (Yuckuza)

- `code/drow_weapons.dm`, `drow_specials.dm`, and `drow_disarm.dm`: drow blades, bardiche, urumi, greatflails, crossbows, shield adjustments, and shared weapon disarming. The hefty greatflail's missing special and the drow urumi's intents are included as dependencies of the port.
- `code/drow_armor.dm` and `drow_scabbards.dm`: drow vest, helmets, mail tights,armor sprites, and modular sheathed-weapon sprites.
- `code/drow_mercenaries.dm`: replaces the existing anthrax drow merc names and lore with the Crocs de l'araignée Cavalier and Assassin.
- `code/drow_adventurer.dm`: adds the drow auxiliary adventurer, with crossbow, sword, or whip training and light or medium armor.
- `code/drow_drider.dm`, and `drow_barding.dm`: Drider mount rework allowing climbing up single z levels + natural armor barding.
- `code/drow_supplies.dm`, `drow_spawner.dm`, and `drow_music.dm`: equipment loot spawner for mappers, merchant catalog harbor stock, and both music tracks.

### Required core edits

- `code/modules/mob/living/ambush.dm`: exempts driders from the timed ambush deaggro deletion that could remove friendly spiders before taming. Prevents Jane Jaluckbreaker from taming a drider ambush spawn only to have it delete itself 44 seconds after it's tamed.
- `code/modules/mob/living/simple_animal/simple_animal.dm`: excludes drider barding from manual removal and equipment overlays.
