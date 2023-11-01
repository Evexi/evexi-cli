
# Evexi CLI

The Evexi CLI helps provides you with some utilities to interact with your Evexi account via our API.



## Installation

Evexi CLI is available for macOS, Windows, and Linux.

### macOS & Linux

Available via [Homebrew](https://brew.sh/):

```sh
brew install evexi/tools/cli
```

### Windows

Available on Windows via [WinGet](https://github.com/microsoft/winget-cli) package manager:

```sh
winget install vexi.EvexiCLI
```
## Usage/Examples

### Player Copy

This commands allows you to copy content, application and variables of a player to other players.

**NOTES**:
- Sensitive variables are skipped
- Variables already present on the target player will be overwritten if present on the source player
- Variables already present on the target player and not on the source player won't be deleted


| Option           | Description                                                                                | Required                          |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------|
| --only           | Comma separated list of properties to copy (content,application,variables). Default to all | No                                |
| --source:id      | ID of the source player                                                                    | If `source:device` not specified  |
| --source:device  | Device ID of the source player                                                             | If `source:id` not specified      |
| --target:ids     | Comma separated IDs of player where to copy properties                                     | If `target:devices` not specified |
| --target:devices | Comma separated Device IDs of players where to copy properties                             | If `target:ids` not specified     |
| --interactive    | Update target players one at a time. User will be prompted to press ENTER to proceed       | No                                |


#### Example copy by player id
```sh
#### By Player ID

```sh
evexi player copy --source:id 000000000000000000000001 --target:ids 000000000000000000000002,000000000000000000000001
```

#### Example copy by player device id

```sh
evexi player copy --source:device 11111111111111111111111111111111 --target:devices 22222222222222222222222222222222,33333333333333333333333333333333
```

## Support

For support, email development@evexi.technology.


## License
Copyright (c) Evexi. All rights reserved.

Licensed under the [Apache License 2.0 license](blob/master/LICENSE).