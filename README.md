### Preview of kenei gui
Short linoria gui
![Preview](https://github.com/RealTonk/library/assets/130735503/3cd445d8-5f6e-4719-9f57-9b2b8720b45f)
### Get start
Let create library
```lua
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/RealTonk/KeepScripts/main/Librarys/Evolution/Moblie/XenonUi.lua"))()
local window = library:new({textsize = 13.5, font = Enum.Font.RobotoMono, name = "Kenei UI", color = Color3.fromRGB(0, 64, 255)})
```
## Create page
```lua
local General = window:page({name = "General"})
```
```lua
local Settings = window:page({name = "Setting"})
```
## Selection
Size is how long the selection 
Side is where you want to make selection left or right
Name is name of selection
```lua
local Select1 = General:section({name = "General", side = "left", size = 300})
local Select2 = General:section({name = "General two", side = "right", size = 300})
```
```lua
local Setting1 = Settings:section({name = "Setting", side = "left", size = 300})
local Setting2 = Settings:section({name = "Setting two", side = "right", size = 300})
```
## Toggles
Name is the name of toggle
def when false the toggle will diabale
def when true the toggle will enable and if put function will enable too

```lua
General:toggle(
    {
        name = "Toggle",
        def = false,
        callback = function(vu)
            getgenv().Toggle = vu
        end
    }
)
```
```lua
Settings:toggle(
    {
        name = "Toggle",
        def = true,
        callback = function(vu)
            getgenv().Toggle = vu
        end
    }
)
```
## Buttons
the name is button name you want to set
```lua
General:button(
    {
        name = "Button",
        callback = function()
            print("Clicked")
        end
    }
)
```
## Silders
This might hard understand.

Set the silders:
```lua
local Default_Verse = 10
local Minimum_Verse = -10
local Maximum_Verse = 30
local Decimals_Verse = 10
```
name of sliders
default is will set as that number
minimum is lowest number can go
maximum is highest number can go

Create the silders:
```lua
General:slider(
    {
        name = "Slider",
        Default = 10,
        Minimum = -10,
        Maximum = 30,
        Decimals = 10,
        Suffix = "%",
        Callback = function(vu)
            getgenv().Slider = vu
        end
,
)
```
```lua
local Default_Verse = 10
local Minimum_Verse = -10
local Maximum_Verse = 30
local Decimals_Verse = 10
General:slider(
    {
        name = "Slider",
        Default = 10,
        Minimum = -10,
        Maximum = 30,
        Decimals = 10,
        Suffix = "%",
        Callback = function(vu)
            getgenv().Slider = vu
        end
    }
)
```

This gui from other! This is only wikis
