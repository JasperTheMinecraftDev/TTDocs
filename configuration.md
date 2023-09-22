# ⚙ Configuration

## Configuration

### Config.yml File

The `config.yml` file contains settings for the plugin. Below are the options available:

#### Round Finish Commands

`round-finish-commands` specifies the commands that will be executed when a round is finished. The commands can be customized for both taggers and survivors. You can use the player placeholder `%player%` in the commands.

Example:

```yaml
round-finish-commands:
  taggers:
    - eco add %player% 10
  survivors:
    - eco add %player% 20
```

#### Arena Finish Commands

`arena-finish-commands` specifies the commands that will be executed when an arena game is finished. You can use the winner placeholder `%winner%` in the command.

Example:

```yaml
arena-finish-commands:
  - eco add %winner% 1000
```

#### Times To Broadcast

`timesToBroadcast` specifies the countdown times when a broadcast message will be sent to the players. You can customize the countdown times to your preference.

Example:

```yaml
timesToBroadcast:
  - 50
  - 40
  - 30
  - 20
  - 15
  - 10
  - 5
  - 4
  - 3
  - 2
  - 1
```

#### Start Message

`startMessage` specifies the message that will be displayed when the game starts. You can customize the message to your preference.

Example:

```yaml
startMessage:
  - "&b==================&cTNT-Tag&b=================="
  - "                    &6&lTNT-Tag        "
  - "   &6You need to avoid the tagger and run fast!        "
  - " &6&lHit someone quickly when you get tagged before you explode!        "
  - "&b==================&cTNT-Tag&b=================="
```

### Arena Configuration File

The arena configuration file contains settings for each individual arena. Below are the options available:

#### Start Location

`startLocation` specifies the starting location for the players in the arena.

Example:

```yaml
arena:
  startLocation:
    world: world
    x: 0
    y: 64
    z: 0
```

#### Lobby Location

`lobbyLocation` specifies the lobby location for the players in the arena.

Example:

```yaml
arena:
  lobbyLocation:
    world: world
    x: 0
    y: 64
    z: 0
```

#### Maximum and Minimum Players

`maxPlayers` and `minPlayers` specify the maximum and minimum number of players allowed in the arena.

Example:

```yaml
arena:
  maxPlayers: 16
  minPlayers: 2
```

#### Potion Effects

`potionEffects` specifies the potion effects that will be applied to players in the arena. You can add multiple potion effects by using the format `<POTIONEFFECT:LEVEL:GROUP>` where `POTIONEFFECT` is the name of the potion effect, `LEVEL` is the strength of the potion effect and `GROUP` specifies which group of players the potion effect will be applied to.

Example:

```yaml
arena:
  potionEffects:
    - SPEED:2:SURVIVORS
    - INSTANT_HEALTH:1:TAGGERS
```

#### Round Duration

`roundDuration` specifies the duration of the round in seconds. You can customize this to your liking.

Example:

`roundDuration: 180`

This sets the round duration to 180 seconds (3 minutes). Players will have to avoid being tagged by the TNT block for the duration of the round. Once the round is finished, the round finish commands specified in the config.yml file will be executed.

It is important to note that the round duration can greatly affect the gameplay experience. If the duration is too short, players may not have enough time to fully enjoy the game. On the other hand, if the duration is too long, the game may become tedious and players may lose interest. It is recommended to experiment with different round durations to find the optimal duration for your players.

**Bungee Mode**

`bungee-mode` controls the behavior of players when they join and leave TNT-Tag in Bungee Mode. You can configure whether players instantly join TNT-Tag, are unable to leave TNT-Tag, and specify the lobby server name.

Example:

```yaml
bungee-mode:
  enabled: false
  lobby-server: "lobby" # The name of your lobby server.
  enter-arena-instantly: false # Only enable this if you only have one arena, it will let players enter that arena directly.
  restart-command: "restart" # Your server will be automatically restarted after an arena ends if "enter-arena-instantly" is set to true.
```

**Cooldown for Tagging Survivors**

`cooldown` specifies the cooldown settings for tagging survivors. You can enable or disable it and set the duration in seconds.

Example:

```yaml
cooldown:
  enabled: true
  duration: 2.0
```

**Delay Settings**

`delay` specifies the delay settings between starting a new round and teleporting back to the global lobby after a game. You can configure the delay for both situations.

Example:

```yaml
delay:
  new-round: 3
  after-game: 5
```

**Global Lobby Option**

`global-lobby` determines whether the global lobby is enabled or disabled. If set to false, players will instantly leave the TNT-Tag mode when they want to leave an arena, and they won't be able to join it as well if this is disabled.

Example:

```yaml
global-lobby: true
```
