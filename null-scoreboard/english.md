# English

## null-scoreboard | FiveM Scoreboard

A modern and responsive scoreboard for the QBCore Framework. It displays server information, a list of available crimes, and your own player information in a stylish and easy-to-read UI. It is easily customizable from the config file and supports multiple languages.

***

### ✨ Main Features

* **Server Info Display**: Shows the number of online players, police officers, and EMS personnel.
* **Your Information Display**: Individually displays your own server ID, name, and ping.
* **Crime List**: Displays a list of crimes configured in `config.lua`.
  * The status (Available/Unavailable) changes in real-time based on the number of required police officers.
  * Features a responsive design that automatically adjusts the width and number of columns based on the item count.
* **Automatic Version Checker**: Automatically checks for new updates on server start and displays a notification in the console.
* **Fully Configurable**: Toggle the visibility of almost all display elements individually from `config.lua`.
* **Flexible Sorting**: The crime list can be sorted by the required number of police in ascending or descending order.
* **Multi-language Support**: Easily add new languages by creating a new file in the `locales` folder. (Comes with English and Japanese by default).
* **Player-configurable Keybinds**: Players can freely change the key to open the scoreboard in their in-game key bindings menu.
* **Lightweight Design**: Idle resource consumption is **0.00ms**, ensuring no impact on server performance.

***

### Preview

_(It is recommended to replace this line with a screenshot of your scoreboard)_

***

### 📥 Installation

1. After purchase, download the `null-scoreboard` zip file from the CFX Keymaster Portal.
2. Extract the zip file and place the `null-scoreboard` folder into your server's `resources` directory.
3.  Open your `server.cfg` file and add the following line:

    ```cfg
    ensure null-scoreboard
    ```
4. Restart your server, and the installation is complete.

***

### ⚙️ Configuration

All settings are managed in the `config.lua` file and the files within the `locales` folder.

#### ### `config.lua`

```lua
Config = {}

-- Set the display language ('en' or 'ja')
Config.Lang = 'en'

-- The default key if the player has not set a custom keybind
Config.DefaultKey = 'Home'

-- Configure the sort order of the crime list
-- 'asc': Ascending by required police count
-- 'desc': Descending by required police count
-- false: The order as written in this file
Config.SortCrimeList = 'asc'

-- Specify the actual job names in QBCore
Config.Job = {
    police = 'police',  
    ambulance = 'ambulance'
}

-- Toggle the visibility of each UI element (true or false)
Config.Display = {
    player = true,      -- Total player count on the server
    police = true,      -- Police officer count
    ambulance = true,   -- EMS count
    id = true,          -- Your own ID
    name = true,        -- Your own name
    ping = true,        -- Your own ping
}

-- The list of crimes to display
Config.crimelist = {
    ['storerobbery'] = {       -- Unique ID for the crime
        label = "Convenience Store Robbery", -- Name displayed in the UI
        minpolice = 2,         -- Minimum number of police required to perform
        status = false         -- Always leave this as false
    },
    -- ...
}

### locales/en.lua (Language File)

All text displayed in the UI can be edited in the language files within the locales folder. To add a new language, you can copy en.lua, create a new file such as es.lua (Spanish), and translate the text inside.

## 💬 Support

For installation questions or bug reports, please join the following Discord server and create a ticket.

    Discord: https://discord.gg/eK94chg27j
```
