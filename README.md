# Spawtify
*A spotify widget for awesome-wm.*

![screenshot](https://github.com/akshat46/spawtify/blob/master/screenshots/spawtify-screenshot.png)

## Usage
Clone the repository in your config file with:

```
git clone https://github.com/akshat46/spawtify.git
```

And add following code to your `rc.lua`: 

```Lua
local spawtify = require("spawtify/spotify_widget")

awful.screen.connect_for_each_screen(function(s)
  ...
  spawtify.widget({
        screen = s, --required
        artwork = true,
    })
  ...
end
```

## Customization

`Screen` parameter is required. Rest optional parameters are: 

```Lua
spawtify.widget({
  screen = s, --required
  artwork = true, --show artwork
  width = 460, 
  height = 600,
  bg = "#000000", -- background color
  bottom_margin = 225, --[[widget's margin from the bottom edge of 
  the screen (will definitely change later on) ]]--
})
```

Note: Currently the widget can only be moved to right edge of the screen. Will add more options once I get time.
