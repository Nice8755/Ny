local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("BlueSky", colors)
Plr = {}
-- OP

local Tab = Window:NewTab("OP")
local OP = Tab:NewSection("OP")

OP:NewKeybind("Key Die", "KeybindInfo", Enum.KeyCode.G, function()
	loadstring(game:HttpGet("https://raw.githubusercontent.com/Nice8755/ASD/main/README.md"))()("You just clicked the bind")
end)


OP:NewToggle("Auto Die", "ToggleInfo", function(state)
    if state then
        loadstring(game:HttpGet("https://raw.githubusercontent.com/Nice8755/zz1/main/README.md"))()("Toggle On")
    else
        loadstring(game:HttpGet("https://raw.githubusercontent.com/Nice8755/die-/main/README.md"))()("Toggle Off")
    end
end)


-- Teleport

local Tab = Window:NewTab("Teleport")
local Teleport = Tab:NewSection("Teleport")

Teleport:NewButton("SafezonePart Store", "", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").GameStuff.SafezonePart.CFrame
end)

Teleport:NewButton("WarningFromTheFutureGokuBlack Lv.100", "", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").GameStuff.WarningFromTheFutureGokuBlackTeleporter.TeleportPart.CFrame
end)

Teleport:NewButton("EternalHorrorBroly Lv.350", "", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").GameStuff.EternalHorrorBrolyTeleporter.TeleportPart.CFrame
end)

Teleport:NewButton("Cooler Lv.400", "", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").GameStuff.CoolerTeleporter.TeleportPart.CFrame
end)

Teleport:NewButton("BlazingClashPikkon Lv.600", "", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").GameStuff.BlazingClashPikkonTeleporter.TeleportPart.CFrame
end)

Teleport:NewButton("BurningFurySuperSaiyanBlueVegeta Lv.700", "", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").GameStuff.BurningFurySuperSaiyanBlueVegetaTeleporter.TeleportPart.CFrame
end)


-- SpeedWalk

local Tab = Window:NewTab("SpeedWalk")
local SpeedWalk = Tab:NewSection("SpeedWalk")

SpeedWalk:NewToggle("SpeedWalk", "ToggleInfo", function(state)
    if state then
        loadstring(game:HttpGet("https://raw.githubusercontent.com/Nice8755/sw/main/README.md"))()("Toggle On")
    else
        loadstring(game:HttpGet("https://raw.githubusercontent.com/Nice8755/sw-/main/README.md"))()("Toggle Off")
    end
end)


-- Teleport Player

local Tab = Window:NewTab("Teleport Player")
local Player = Tab:NewSection("Teleport Player")

for i,v in pairs(game:GetService("Players"):GetChildren()) do
    table.insert(Plr,v.Name) 
end
local drop = Player:NewDropdown("Select Player!", "Click To Select", Plr, function(t)
   PlayerTP = t
end)
Player:NewButton("Click To TP", "", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
end)
Player:NewToggle("Auto Tp", "", function(t)
_G.TPPlayer = t
while _G.TPPlayer do wait()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
end
end)


-- Credit

local Tab = Window:NewTab("Credit")
local Credit = Tab:NewSection("BlueSkyNy")

Credit:NewKeybind("Hidden", "KeybindInfo", Enum.KeyCode.Insert, function()
	Library:ToggleUI()
end)


loadstring(game:HttpGet(('https://raw.githubusercontent.com/XTheMasterX/Scripts/Main/dbzadventuresunleashed'),true))()
