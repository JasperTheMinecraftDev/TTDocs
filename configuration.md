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
