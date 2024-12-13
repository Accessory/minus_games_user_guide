# Minus Games
Minus Games is a Suite to Distribute Games from a server to a client. It consists of the 5 applications:

- [Minus Games Server](./minus_games_server/minus_games_server.md)
- [Minus Games Client](./minus_games_client/minus_games_client.md)
- [Minus Games Gui](./minus_games_gui/minus_games_gui.md)
- [Minus Games Finder](./minus_games_finder/minus_games_finder.md)
- [Minus Games Updater](./minus_games_updater/minus_games_updater.md)

To get everything up and running see the [Quick Start Guide](quick_start/quick_start.md)

## FAQ
### What is the main use case?
The main use case is to distribute games and save files from the server to the clients
in a home server environment.

### What is the main advantage of Minus Games?
Minus Games does not just keep the game files in sync with the server,
it is also capable to sync save files.

### What was the main motivation to create Minus Games?
I wanted a way to sync save games between my Steamdeck and my Desktop PC
for games that are not managed by Steam or other game launchers.

### What is the main way to use the Minus Games?
The main way is to start configure the server and put the games in the designated game folder.
After that, let the server search for new files by calling the `/finder/rerun-finder` endpoint.

The server will scan for new games and make them available for the client.
The client now can download the games and run them.

If the game has a known engine like Unity. It will check for save files.
The sync of the save files is done by the client. For a full Quick Start see the 
[Quick Start Guide](quick_start/quick_start.md)