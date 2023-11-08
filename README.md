
# Evexi CLI

The Evexi CLI helps provides you with some utilities to interact with your Evexi account via our API.



## Installation

Evexi CLI is available for macOS, Windows, and Linux.

### macOS & Linux

Available via [Homebrew](https://brew.sh/):

```sh
brew install evexi/tools/evexi-cli
```

### Windows

Available via [WinGet](https://github.com/microsoft/winget-cli) package manager:

```sh
winget install Evexi.EvexiCLI
```

## Usage/Examples



### Player Copy

This commands allows you to copy content, application and variables of a player to other players.

**NOTES**:
- Sensitive variables are skipped
- Variables already present on the target player will be overwritten if present on the source player
- Variables already present on the target player and not on the source player won't be deleted


| Option                               	| Description                                                                                                                                                                                                                                          	| Default                       	| Required 	|
|--------------------------------------	|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|-------------------------------	|----------	|
| --source:id **or** --source:device   	| Specify either the source player ID which can be seen in the browser URL when viewing the player on admin<br>**or**<br>device ID which can be seen when viewing the player detail on admin or on the actual screen                                   	| -                             	| Yes      	|
| --target:ids **or** --target:devices 	| Specify a comma separated list of either the target player IDs which can be seen in the browser URL when viewing the players on admin <br>**or** <br>device IDs which can be seen when viewing the players' detail on admin or on the actual screens 	| -                             	| Yes      	|
| --only                               	| Specify a comma separated list of properties to copy from the source player<br><br>Values: content,application,variables                                                                                                                             	| content,application,variables 	| No       	|
| --interactive                        	| Specify whether to execute the copy one target player at a time<br><br>User will be prompted to press ENTER to proceed                                                                                                                               	| false                         	| No       	|
| --help                               	| Show command help                                                                                                                                                                                                                                    	| false                         	| No       	|


#### Example copy by player id

```sh
evexi player copy --source:id 000000000000000000000001 --target:ids 000000000000000000000002,000000000000000000000001
```

#### Example copy by player's device id

```sh
evexi player copy --source:device 11111111111111111111111111111111 --target:devices 22222222222222222222222222222222,33333333333333333333333333333333
```

## Support

For support, email development@evexi.technology.


## License
Copyright (c) Evexi. All rights reserved.

Licensed under the [Apache License 2.0 license](blob/master/LICENSE).