# 💬 API

Here is a possible TNT-Tag API page:

## TNT-Tag API

To use the TNT-Tag API, call `Tnttag.getAPI()`, which returns an instance of the `API` class. The `API` class provides the following methods:

### Methods

#### `int getTimesTagged(UUID playerUUID)`

Returns the number of times the specified player has been tagged.

#### `int getWins(UUID playerUUID)`

Returns the number of times the specified player has won a game.

#### `int getTags(UUID playerUUID)`

Returns the number of times the specified player has tagged other players.

#### `void setTimesTagged(UUID playerUUID, int value)`

Sets the number of times the specified player has been tagged.

#### `void setWins(UUID playerUUID, int value)`

Sets the number of times the specified player has won a game.

#### `void setTags(UUID playerUUID, int value)`

Sets the number of times the specified player has tagged other players.

#### `boolean arenaExists(String arenaName)`

Returns true if the specified arena exists.

#### `HashMap<Player, PlayerType> getPlayers(String arenaName)`

Returns a map of the players in the specified arena and their types (TNT or player).

#### `String getArenaState(String arenaName)`

Returns the current state of the specified arena (WAITING, STARTING, RUNNING, or ENDING).

#### `TreeMap<UUID, Integer> getWinsData()`

Returns a map of the UUIDs of all players and their corresponding number of wins.

#### `TreeMap<UUID, Integer> getTimesTaggedData()`

Returns a map of the UUIDs of all players and their corresponding number of times tagged.

#### `TreeMap<UUID, Integer> getTagsData()`

Returns a map of the UUIDs of all players and their corresponding number of tags.

### Events

The following events are available:

#### `ArenaEndingEvent`

**Methods**

* `String getArenaName()`: Returns the name of the arena that is ending.
* `HashMap<Player, PlayerType> getPlayers()`: Returns a map of the players in the arena and their types (TNT or player).
* `ArrayList<Player> getWinners()`: Returns a list of the players who won the game.

#### `ArenaStartedEvent`

**Methods**

* `String getArenaName()`: Returns the name of the arena that has started.

#### `ArenaStartingEvent`

**Methods**

* `String getArenaName()`: Returns the name of the arena that is starting.

#### `PlayerJoinArenaEvent`

**Methods**

* `Player getPlayer()`: Returns the player who joined the arena.
* `String getArenaName()`: Returns the name of the arena the player joined.

#### `PlayerLeaveArenaEvent`

**Methods**

* `Player getPlayer()`: Returns the player who left the arena.
* `String getArenaName()`: Returns the name of the arena the player left.

#### `PlayerLostRoundEvent`

**Methods**

* `Player getPlayer()`: Returns the player who lost the round.
* `String getArenaName()`: Returns the name of the arena where the player lost.
