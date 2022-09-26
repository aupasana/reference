# Creating system hotkeys with hammerspoon

Add this to `~/.hammerspoon/init.lua` to toogle alacritty with opt-space:

```lua
hs.hotkey.bind({"alt"}, "space", function()
  local alacritty = hs.application.find('alacritty')
  if alacritty:isFrontmost() then
    alacritty:hide()
  else
    hs.application.launchOrFocus("/Applications/Alacritty.app")
  end
end)
```

Source: https://github.com/alacritty/alacritty/issues/862
