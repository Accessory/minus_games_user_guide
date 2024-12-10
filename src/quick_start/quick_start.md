# Quickstart

## Step 1: Set up the Minus Games Server

### Setup
For a quick and easy installation, it is recommended to have the `minus_games_server` executable, the data, and the games folder in one directory.

The server can be configured by command line args or by a **.env** file.
An example **.env** file can look like this:

```
# default ip is 127.0.0.1 
# IP=0.0.0.0 
# default port is 8415
# PORT=8415
DATA_FOLDER=data
GAMES_FOLDER=games
```

This would result in an initial layout like this.

```
.
├── minus_games_server      # Main executable
├── .env                    # Server configuration file
├── games                   # Documentation files (alternatively `doc`)
    ├── Game 1              # Every game has its own folder
    ├── Game 2              
    ├── ...               
├── data                    # Folder for the games metadata (created by the finder or the server)
├── users                   # Folder for the user configuration
```

After setting up the games and the config, you can simply run the server with `./minus_games_server` (or `.\minus_games_server.exe` under Windows).

This will run the server and expose the OpenAPI and the Swagger UI under `http://[your-server]:[your-port]/swagger-ui` -> defaults to `http://localhost:8415/swagger-ui`.

### Add Game
To add a game, copy the main folder of the game into the games folder.
After that, you can visit the swagger-ui and run the finder/rerun-finder endpoint.
Alternatively, you can use the minus_games_finder to create the needed metadata.

## Step 2: Set up the Minus Games Gui

The GUI can be set up in nearly the same way as the server.
The easiest way to configure the GUI is by adding a .env file.
It is also possible to configure everything within the GUI under Settings.

Example **.env** file:
```
# When running under linux a wine be used and set up by setting the WINE_EXE and WINE_PREFIX environment variable.
# The server url defaults to localhost if not specified
# SERVER_URL="http://localhost:8415"
CLIENT_GAMES_FOLDER=client_games
CLIENT_FOLDER=client_data
```

The order in witch the configuration is applied is: 
1. Command line args
2. .env file
3. Config File

Higher priority settings will overwrite lower priority settings.

This setup will result in a GUI folder layout like this:

```
.
├── minus_games_client      # Main executable
├── .env                    # Client configuration file
├── client_games            # Documentation files (alternatively `doc`)
    ├── Game 1              # Every game has its own folder
    ├── Game 2              
    ├── ...               
├── client_data             # Folder for the games metadata (created by the finder or the server)
```

To run the GUI, make sure the server is running and that the server points at the server.
The GUI can run downloaded games offline, but it will not be possible to sync saves or download games.

Now run the GUI with:

```
./minus_games_gui

# Or under windows
#.\minus_games_gui.exe
```

To Download a game run and sync it just select the first option.
The Gui will lookup the games that are already installed and the games that are available on the server.
Now you can select a game from a that list and run it.