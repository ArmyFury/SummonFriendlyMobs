# Summon Friendly Mobs

## A minecraft plugin which allows you to summon hostile mobs which do not attack the player who summoned it.

### Downloads: [Modrinth](https://modrinth.com/plugin/summonfriendlymobs)

### Commands Usage:

```MCFUNCTION
/summonfriendlymob <mob_type> [<x> <y> <z>} {NBT_data} # Summons a friendly mob

/givespawnegg <player> <mob_type> [amount] # Gives special spwan egg to a player

/attack <target player name | target mob uuid> # Attacks given player or a mob

/mobs # Gives a list of friendly mobs of the player 

/sfmreload # Reload the plugin
```

### Alias:

/sfm               [for summonfriendlymob]

/gse               [for givespawnegg]

only put mob **NAME** in <mob_type>.

Example:
```MCFUNCTION
   ✅ /summonfriendlymob blaze
   ✅ /sfm blaze
   ✅ /givespecialspawnegg @s blaze
   ✅ /gse @s blaze

   
   ❌ /summonfriendlymob minecraft:blaze
   ❌ /sfm minecraft:blaze
   ❌ /givespecialspawnegg minecraft:blaze
   ❌ /gse minecraft:blaze
```

Coordinates are optional, when none are given, it defaults to ~ ~ ~
Amount is also optional, defaults to 1 when not specified

### Configurations

**For versions below 1.19.x, if the config file is not properly generated the first time, restart the server.**

The config file (config.yml) can be found in _`<server_folder>/plugins/SummonFriendlyMobs/`_ .
You can change _FriendlyWarden (MC 1.19+), UniversallyFriendly, SaveFriendliness, SaveWardenFriendliness, WardenCheckInterval (MC 1.19+), UpdateNotifier, AllowAttack and AllowCustomMobSettings_ in the config.

```YAML
FriendlyWarden: false # Toggle whether wardens summoned by the plugin are friendly to the summoner.
WardenCheckInterval: 1 # Number of ticks between each check to clear Warden's anger to its summoner
UniversallyFriendly: false # Toggle whether mobs summoned by this plugin are Friendly to only the summoner or to all player
SaveFriendliness: false # Toggle whether to keep friendliness of the mobs even after the server restarts
SaveWardenFriendliness: false # Toggle whether to keep friendliness of the wardens even after the server restarts
UpdateNotifier: true # Toggle whether to notify for newer versions of the plugin
AllowAttack: true # Toggle whether to allow players to use /attack command or not
AllowCustomMobSettings: false # Toggle whether to use settings for mobs from mobs.yml or not
```

`WardenCheckInterval` is the number of ticks after which anger of wardens is cleared, higher number will result in lower number of checks and the wardens may attack the summoners. This should not affect the performance a lot. This does not apply to any other mob. Wardens are pacified differently due to how they sense and attack players.

The file `summonerMap.dat` holds data for friendliness of mobs and `warden_data.yml` for friendliness of wardens. DO NOT change anything in them unless you are 100% sure what you are doing

### Permissions

  - summonfriendlymob.summon : Permission required to use /summonfriendlymob or /sfm command
  - summonfriendlymob.give : Permission required to use /givespawnegg or /gse command
  - summonfriendlymob.attack : Permission required to use /attack command
  - summonfriendlymob.check : Permission required to use /mobs command
  - summonfriendlymob.reload : Permission required to use /sfmreload command

### Issues
 I know there are and will be some issues in this plugin as this is my first ever plugin that I have publically released


Some mobs are hostile even to the players who summoned them:
  - Warden (Fixed in versions 2.0 and above)
  - Zoglin
  - Pufferfish (Fixed in 3.0+)
  - Ender Dragon 
  - Guardian & Elder Guardian (Thorns) (Fixed in 2.1)
  - Any mob which was originally not hostile but got converted to a different mob (example: non hostile zombie converts to hostile drowned) (Fixed in 2.1)
  - Initial slime/magma cube which is spawned is not hostile but the offsprings of the slime/magma cube are hostile


You can reach out to me in my [discord server](https://discord.gg/aEc7yqecYn). [Discord ID - armyfury]

### Other projects:
  - [WoolBurner](https://modrinth.com/plugin/woolburner)
