# Minus Games Client

## Configuration Options

| Option                  | Description                                      | Default                  | Environment Variable       | Command Line Argument          |
|-------------------------|--------------------------------------------------|--------------------------|----------------------------|---------------------------------|
| **server\_url**         | The URL of the server.                           | `http://127.0.0.1:8415`  | `SERVER_URL`               | `--server-url`                 |
| **client\_folder**      | The folder where client data is stored.          | Client folder            | `CLIENT_FOLDER`            | `--client-folder`              |
| **wine\_exe**           | The path to the Wine executable (optional).      | None                     | `WINE_EXE`                 | `--wine-exe`                   |
| **wine\_prefix**        | The path to the Wine prefix (optional).          | None                     | `WINE_PREFIX`              | `--wine-prefix`                |
| **verbose**             | Enable verbose output.                           | `false`                  | `VERBOSE`                  | `-v` or `--verbose`            |
| **offline**             | Run in offline mode.                             | `false`                  | `OFFLINE`                  | `-o` or `--offline`            |
| **client\_games\_folder** | The folder where client games are stored.      | Current directory        | `CLIENT_GAMES_FOLDER`      | `--client-games-folder`        |
| **username**            | The username for authentication (optional).      | None                     | `MINUS_GAMES_USERNAME`     | `--username`                   |
| **password**            | The password for authentication (optional).      | None                     | `MINUS_GAMES_PASSWORD`     | `--password`                   |
| **action**              | The action to perform.                           | None                     | None                       | Subcommands like `list`, `download`, `sync`, etc. |

### Actions

| Action              | Description                                           | Command Line Argument     | Additional Value Needed |
|---------------------|-------------------------------------------------------|---------------------------|-------------------------|
| **List**            | Lists all available games.                            | `list`                    | None                    |
| **ListJson**        | Lists all available games in JSON format.             | `list-json`               | None                    |
| **Download**        | Downloads the specified game.                         | `download`                | `game`                  |
| **Sync**            | Synchronizes information for all games.               | `sync`                    | None                    |
| **SelectDownload**  | Prompts the user to select a game to download.        | `select-download`         | None                    |
| **RunGame**         | Runs the specified game.                              | `run-game`                | `game`                  |
| **RunGameSynced**   | Runs the specified game with synchronization.         | `run-game-synced`         | `game`                  |
| **SyncRunGame**     | Synchronizes and runs the specified game.             | `sync-run-game`           | `game`                  |
| **SelectGame**      | Prompts the user to select a game.                    | `select-game`             | None                    |
| **DeleteGame**      | Deletes the specified game, optionally purging it.    | `delete-game`             | `game`, `purge`         |
| **SelectDeleteGame**| Prompts the user to select a game to delete, optionally purging it.| `select-delete-game` | `purge`                 |
| **Menu**            | Displays the main menu.                               | `menu`                    | None                    |
| **Repair**          | Repairs the specified game.                           | `repair`                  | `game`                  |
| **SelectRepair**    | Prompts the user to select a game to repair.          | `select-repair`           | None                    |
| **DownloadSyncs**   | Downloads synchronization data for all games.         | `download-syncs`          | None                    |
| **DownloadSync**    | Downloads synchronization data for the specified game.| `download-sync`           | `game`                  |
| **UploadSyncs**     | Uploads synchronization data for all games.           | `upload-syncs`            | None                    |
| **ScanForGames**    | Scans for installed games.                            | `scan-for-games`          | None                    |
| **SelectGameToPlay**| Prompts the user to select a game to play (only on Unix systems).| `select-game-to-play` | None                    |
