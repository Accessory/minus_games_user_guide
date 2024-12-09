# Minus Games Gui

## Configuration Options

The **Minus Games Gui** uses the same options as the **Minus Games Client** and
if the mode is set to **Cli** the Gui will behave like the client.

| Option                  | Description                                      | Default            | Environment Variable       | Command Line Argument          |
|-------------------------|--------------------------------------------------|--------------------|----------------------------|---------------------------------|
| **fullscreen**          | Whether to run in fullscreen mode.               | `false`            | `MINUS_GAMES_GUI_FULLSCREEN`| `--fullscreen`                 |
| **mode**                | The mode to run the GUI in.                      | `Gui`              | `MINUS_GAMES_GUI_MODE`     | `--mode`                       |
| **theme**               | The theme of the GUI.                            | `Light`            | `MINUS_GAMES_GUI_THEME`    | `--theme`                      |
| **server\_url**         | The URL of the server.                           | `http://127.0.0.1:8415`  | `SERVER_URL`               | `--server-url`                 |
| **client\_folder**      | The folder where client data is stored.          | Client folder            | `CLIENT_FOLDER`            | `--client-folder`              |
| **wine\_exe**           | The path to the Wine executable (optional).      | None                     | `WINE_EXE`                 | `--wine-exe`                   |
| **wine\_prefix**        | The path to the Wine prefix (optional).          | None                     | `WINE_PREFIX`              | `--wine-prefix`                |
| **verbose**             | Enable verbose output.                           | `false`                  | `VERBOSE`                  | `-v` or `--verbose`            |
| **offline**             | Run in offline mode.                             | `false`                  | `OFFLINE`                  | `-o` or `--offline`            |
| **client\_games\_folder** | The folder where client games are stored.      | Current directory        | `CLIENT_GAMES_FOLDER`      | `--client-games-folder`        |
| **username**            | The username for authentication (optional).      | None                     | `MINUS_GAMES_USERNAME`     | `--username`                   |
| **password**            | The password for authentication (optional).      | None                     | `MINUS_GAMES_PASSWORD`     | `--password`                   |
