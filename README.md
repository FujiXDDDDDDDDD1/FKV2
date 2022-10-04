local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Fu Kang Hub V2", "BloodTheme")

local Tab = Window:NewTab("Main")
local Section = Tab:NewSection("Main")

Section:NewButton("Fu Kang", "IY Admin", function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
end)

Section:NewButton("RTX ON", "Fu Kang", function()
    getgenv().mode = "Summer" -- Choose from Summer and Autumn




local a = game.Lighting
a.EnvironmentSpecularScale = 0.522
a.GlobalShadows = true
a.Ambient = Color3.fromRGB(33, 33, 33)
a.Brightness = 6.67
a.ColorShift_Bottom = Color3.fromRGB(0, 0, 0)
a.ColorShift_Top = Color3.fromRGB(255, 247, 237)
a.EnvironmentDiffuseScale = 0.105
a.OutdoorAmbient = Color3.fromRGB(51, 54, 67)
a.ShadowSoftness = 0.04
a.GeographicLatitude = -15.525
a.ExposureCompensation = 0.75
local b = Instance.new("BloomEffect", a)
b.Enabled = true
b.Intensity = 0.04
b.Size = 1900
b.Threshold = 0.915
local c = Instance.new("ColorCorrectionEffect", a)
c.Brightness = 0.176
c.Contrast = 0.39
c.Enabled = true
c.Saturation = 0.2
c.TintColor = Color3.fromRGB(217, 145, 57)
if getgenv().mode == "Summer" then
   c.TintColor = Color3.fromRGB(255, 220, 148)
elseif getgenv().mode == "Autumn" then
   c.TintColor = Color3.fromRGB(217, 145, 57)
else
   warn("No mode selected!")
   print("Please select a mode")
   b:Destroy()
   c:Destroy()
end
local d = Instance.new("DepthOfFieldEffect", a)
d.Enabled = true
d.FarIntensity = 0.077
d.FocusDistance = 21.54
d.InFocusRadius = 20.77
d.NearIntensity = 0.277
local e = Instance.new("ColorCorrectionEffect", a)
e.Brightness = 0
e.Contrast = -0.07
e.Saturation = 0
e.Enabled = true
e.TintColor = Color3.fromRGB(255, 247, 239)
local e2 = Instance.new("ColorCorrectionEffect", a)
e2.Brightness = 0.2
e2.Contrast = 0.45
e2.Saturation = -0.1
e2.Enabled = true
e2.TintColor = Color3.fromRGB(255, 255, 255)
local s = Instance.new("SunRaysEffect", a)
s.Enabled = true
s.Intensity = 0.01
s.Spread = 0.146

print("RTX On ละควาย")
end)

Section:NewButton("FPS Boost", "Fu Kang", function()
    local decalsyeeted = true 
local g = game
local w = g.Workspace
local l = g.Lighting
local t = w.Terrain
sethiddenproperty(l,"Technology",2)
sethiddenproperty(t,"Decoration",false)
t.WaterWaveSize = 0
t.WaterWaveSpeed = 0
t.WaterReflectance = 0
t.WaterTransparency = 0
l.GlobalShadows = 0
l.FogEnd = 9e9
l.Brightness = 0
settings().Rendering.QualityLevel = "Level01"
for i, v in pairs(w:GetDescendants()) do
    if v:IsA("BasePart") and not v:IsA("MeshPart") then
        v.Material = "Plastic"
        v.Reflectance = 0
    elseif (v:IsA("Decal") or v:IsA("Texture")) and decalsyeeted then
        v.Transparency = 1
    elseif v:IsA("ParticleEmitter") or v:IsA("Trail") then
        v.Lifetime = NumberRange.new(0)
    elseif v:IsA("Explosion") then
        v.BlastPressure = 1
        v.BlastRadius = 1
    elseif v:IsA("Fire") or v:IsA("SpotLight") or v:IsA("Smoke") or v:IsA("Sparkles") then
        v.Enabled = false
    elseif v:IsA("MeshPart") and decalsyeeted then
        v.Material = "Plastic"
        v.Reflectance = 0
        v.TextureID = 10385902758728957
    elseif v:IsA("SpecialMesh") and decalsyeeted  then
        v.TextureId=0
    elseif v:IsA("ShirtGraphic") and decalsyeeted then
        v.Graphic=0
    elseif (v:IsA("Shirt") or v:IsA("Pants")) and decalsyeeted then
        v[v.ClassName.."Template"]=0
    end
end
for i = 1,#l:GetChildren() do
    e=l:GetChildren()[i]
    if e:IsA("BlurEffect") or e:IsA("SunRaysEffect") or e:IsA("ColorCorrectionEffect") or e:IsA("BloomEffect") or e:IsA("DepthOfFieldEffect") then
        e.Enabled = false
    end
end
w.DescendantAdded:Connect(function(v)
    wait()--prevent errors and shit
   if v:IsA("BasePart") and not v:IsA("MeshPart") then
        v.Material = "Plastic"
        v.Reflectance = 0
    elseif v:IsA("Decal") or v:IsA("Texture") and decalsyeeted then
        v.Transparency = 1
    elseif v:IsA("ParticleEmitter") or v:IsA("Trail") then
        v.Lifetime = NumberRange.new(0)
    elseif v:IsA("Explosion") then
        v.BlastPressure = 1
        v.BlastRadius = 1
    elseif v:IsA("Fire") or v:IsA("SpotLight") or v:IsA("Smoke") or v:IsA("Sparkles") then
        v.Enabled = false
    elseif v:IsA("MeshPart") and decalsyeeted then
        v.Material = "Plastic"
        v.Reflectance = 0
        v.TextureID = 10385902758728957
    elseif v:IsA("SpecialMesh") and decalsyeeted then
        v.TextureId=0
    elseif v:IsA("ShirtGraphic") and decalsyeeted then
        v.ShirtGraphic=0
    elseif (v:IsA("Shirt") or v:IsA("Pants")) and decalsyeeted then
        v[v.ClassName.."Template"]=0
    end
end)
print("Boost ให้ละSiuu")
end)

Section:NewButton("Avatar", "Fu Kang", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/FujiXDDDDDDDDD1/Animation-FK/main/README.md"))();
end)

Section:NewButton("Animation", "Fu Kang", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/FujiXDDDDDDDDD1/FujiXDDDDDDDDD1/main/README.md"))();
end)

Section:NewButton("D4z Hub", "Fu Kang", function()
    print("D4z Hub ไม่มีหลอกโง่ มีเเต่ Fu Kang Hub V2 ที่เร็วๆนี้จะมา")
end)

Section:NewButton("Fullbright", "Fu Kang", function()
    loadstring(game:HttpGet("https://pastebin.com/raw/06iG6YkU", true))()
end)

Section:NewButton("Anti AFK", "Fu Kang", function()
    wait(0.5)local ba=Instance.new("ScreenGui")
local ca=Instance.new("TextLabel")local da=Instance.new("Frame")
local _b=Instance.new("TextLabel")local ab=Instance.new("TextLabel")ba.Parent=game.CoreGui
ba.ZIndexBehavior=Enum.ZIndexBehavior.Sibling;ca.Parent=ba;ca.Active=true
ca.BackgroundColor3=Color3.new(0.176471,0.176471,0.176471)ca.Draggable=true
ca.Position=UDim2.new(0.698610067,0,0.098096624,0)ca.Size=UDim2.new(0,304,0,52)
ca.Font=Enum.Font.SourceSansSemibold;ca.Text="Anti Afk Kick Script"ca.TextColor3=Color3.new(0,1,1)
ca.TextSize=22;da.Parent=ca
da.BackgroundColor3=Color3.new(0.196078,0.196078,0.196078)da.Position=UDim2.new(0,0,1.0192306,0)
da.Size=UDim2.new(0,304,0,107)_b.Parent=da
_b.BackgroundColor3=Color3.new(0.176471,0.176471,0.176471)_b.Position=UDim2.new(0,0,0.800455689,0)
_b.Size=UDim2.new(0,304,0,21)_b.Font=Enum.Font.Arial;_b.Text="Made by Discord: Fu Kang#9999"
_b.TextColor3=Color3.new(1,1,1)_b.TextSize=20;ab.Parent=da
ab.BackgroundColor3=Color3.new(0.176471,0.176471,0.176471)ab.Position=UDim2.new(0,0,0.158377379,0)
ab.Size=UDim2.new(0,304,0,44)ab.Font=Enum.Font.ArialBold;ab.Text="Status: Script Started"
ab.TextColor3=Color3.new(1,1,1)ab.TextSize=20;local bb=game:service'VirtualUser'
game:service'Players'.LocalPlayer.Idled:connect(function()
bb:CaptureController()bb:ClickButton2(Vector2.new())
ab.Text="You went idle and ROBLOX tried to kick you but we reflected it!"wait(2)ab.Text="Script Re-Enabled"end)
end)

Section:NewButton("CTRL+CLICK TP", "Fu Kang", function()
    local Plr = game:GetService("Players").LocalPlayer
 
local Mouse = Plr:GetMouse()
 
 
 
Mouse.Button1Down:connect(function()
 
if not game:GetService("UserInputService"):IsKeyDown(Enum.KeyCode.LeftControl) then return end
 
if not Mouse.Target then return end
 
Plr.Character:MoveTo(Mouse.Hit.p)
 
end)
end)

Section:NewButton("Rejoin Servers", "Fu Kang Hub", function()
    loadstring(game:HttpGet("https://pastebin.com/raw/1gtVMUz3"))()
end)

local Tab = Window:NewTab("Script")
local Section = Tab:NewSection("Blox Fruits")

Section:NewButton("Blox Fruits Hack 1", "Fu Kang Hub V2", function()
    _G.Color = Color3.fromRGB(255, 0, 0)
_G.Color2 = Color3.fromRGB(0, 0, 0)
loadstring(game:HttpGet("https://raw.githubusercontent.com/FujiXDDDDDDDDD1/Fu-Kang-Hub-V2/main/README.md"))();
end)

Section:NewButton("Blox Fruits Hack 2", "Hyper", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/DookDekDEE/Hyper/main/script.lua"))()
end)

Section:NewButton("Teleport 1 (ของโลก 3)", "Fu Kang Hub", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-12463.6025, 376.331696, -7566.08301, 1, 0, -0, 0, 1, 0, 0, 0, 1)
end)

Section:NewButton("Teleport 2 (ของโลก 3)", "Fu Kang Hub", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5089.66455, 316.506805, -3146.12671, 1, 0, -0, 0, 1, 0, 0, 0, 1)
end)

Section:NewButton("Teleport 3 (ของโลก 3)", "Fu Kang Hub", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5099.02441, 316.506805, -3169.30835, 1, 0, -0, 0, 1, 0, 0, 0, 1)
end)

local Section = Tab:NewSection("King Legacy")

Section:NewButton("King Legacy Hack", "Dolce Hub", function()
    loadstring(game:HttpGet"https://raw.githubusercontent.com/xQuartyx/DonateMe/main/ScriptLoader")()
end)

local Section = Tab:NewSection("All Star Tower Defense")

Section:NewButton("All Star Tower Defense Hack", "RIVER HUB", function()
    pcall(function()
        loadstring(game:HttpGet("http://riverhub.xyz/" .. tostring(game.PlaceId) .. ".lua"))()
     end)
end)

local Section = Tab:NewSection("Grand Piece Online")

Section:NewButton("Grand Piece Online Hack", "CFA HUB", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/CFA-HUB/CFA-HUB/main/cfahubfree.lua"))()
end)

local Section = Tab:NewSection("Da Hood")

Section:NewButton("Da Hood Hack", "NOOB HUB", function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/NOOBHUBX/Da-hood/main/NOOB%20HUB.Lua'))()
end)

local Section = Tab:NewSection("Phantom Forces")

Section:NewButton("Phantom Forces Hack", "STRAWHOOK", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/VoidMasterX/strawhook/main/script.lua", true))()
end)

local Section = Tab:NewSection("Arsenal")

Section:NewButton("Arsenal Hack", "V.G HUB", function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/1201for/V.G-Hub/main/V.Ghub'))()
end)

local Section = Tab:NewSection("Mad City")

Section:NewButton("Mad City Hack (Auto Rob)", "MadcityFarm", function()
    loadstring(game:HttpGet('https://scripts.luawl.com/11900/MadcityFarm.lua'))()
end)

Section:NewButton("Mad City Hack (Auto Exp)", "MadcityFarm", function()
    getgenv().key = 'Frost_27824375'
loadstring(game:HttpGet("https://raw.githubusercontent.com/Brizzy9999/scripts/main/madcityxpfarm"))()
end)

Section:NewButton("Key : Brizzy_84792975", "Fu Kang Hub", function()
end)

local Section = Tab:NewSection("DOORS")

Section:NewButton("DOORS Hack", "Fu Kang Hub", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Xfuking/DOORS/main/README.md"))();
end)

local Section = Tab:NewSection("noob fps kaoThapGG")
Section:NewButton("noob fps Hack", "Fu Kang Hub", function()
    getgenv().Main = loadstring(game:HttpGet("https://raw.githubusercontent.com/SuperGamingBros4/Roblox-HAX/main/Better_UI_Library.lua"))()
 
local camera = game:GetService("Workspace").CurrentCamera 
local Plr = game:GetService("Players").LocalPlayer
local RS = game:GetService("RunService")
local mouse = Plr:GetMouse()
 
function getclosestplayertomouse()
    local Target = nil
    for i,v in pairs(game:GetService("Players"):GetPlayers()) do
        if v.Character then
            if v.Character:FindFirstChild("Humanoid") and v.Character:FindFirstChild("Humanoid").Health ~= 0 and v.Character:FindFirstChild("HumanoidRootPart") and v.TeamColor ~= Plr.TeamColor then
                local pos, vis = camera:WorldToViewportPoint(v.Character.HumanoidRootPart.Position)
                local dist = (Vector2.new(mouse.X, mouse.Y) - Vector2.new(pos.X, pos.Y)).Magnitude
                if Main.Flags.VisCheck then
                    if Main.Flags.Size > dist and vis then
                        Target = v
                        print(dist)
                    end
                else
                    if Main.Flags.Size > dist then
                        Target = v
                    end
                end
            end
        end
    end
    return Target
end
 
local circle = Drawing.new("Circle")
circle.Thickness = 0.1
RS.RenderStepped:Connect(function()
    local Settings = Main.Flags
 
    if Settings.Aimbot and Settings.FovCircle then -- FovCircle
        circle.Visible = true
        circle.Color = Color3.fromRGB(Settings.FovRed, Settings.FovGreen, Settings.FovBlue)
        circle.NumSides = Settings.Smoothing
        circle.Radius = Settings.Size
	    circle.Position = Vector2.new(mouse.X, mouse.Y + 35)
    else
        circle.Visible = false
    end
 
    if Settings.Aimbot then -- Aimbot
        for i,arrow in pairs(game:GetService("Workspace"):GetChildren()) do
            if arrow.Name == "arrow" or arrow.Name == "crossbow_arrow" then
                pcall(function()
                    arrow:WaitForChild("Handle").Position = getclosestplayertomouse().Character.HumanoidRootPart.Position
                end)
            end
        end
    end
    if Main.Flags.Speed then -- Toggle Speed
        pcall(function() Plr.Character.Humanoid.WalkSpeed = 22 end)
    end
end)
 
local function InvisPlayer()
    getgenv().InvisRunning = false
    wait(0.01)
    getgenv().InvisRunning = true
    pcall(function()
        local CFrame = Plr.Character.UpperTorso.CFrame
        Plr.Character.HumanoidRootPart:BreakJoints()
        while InvisRunning do
            Plr.Character.UpperTorso.CFrame = CFrame
            wait(0.000001)
        end
    end)
end
 
coroutine.wrap(function()
    while true do
        wait(1)
        if Main.Flags.InstantBreak then -- InstantBreak
            for i,block in pairs(game:GetService("Workspace").Map.Blocks:GetChildren()) do
                block:SetAttribute("Health", 1) 
            end
        end
    end
end)()
local Window = Main:CreateWindow("Fu Kang Hub")
local MainTab = Window:AddTab("Main") do
    MainTab:AddToggle({Name = "Aimbot", Flag = "Aimbot"})
    MainTab:AddToggle({Name = "AimBot Circle", Flag = "FovCircle"})
    MainTab:AddToggle({Name = "VisCheck", Flag = "VisCheck"})
    MainTab:AddSlider({Name = "Aimbot Fov", Default = 50, Max = 500, Flag = "Size"})
    MainTab:AddToggle({Name = "Toggle Sprint", Flag = "Speed"})
    MainTab:AddToggle({Name = "Instant Break", Flag = "InstantBreak"})
    MainTab:AddText("To get out of invisibility, just reset.")
    MainTab:AddButton({Name = "Invisibility", Callback = InvisPlayer})
end
local SettingsTab = Window:AddTab("Settings") do
    SettingsTab:AddText("Fov Circle Settings")
    SettingsTab:AddSlider({Name = "Red", Flag = "FovRed", Default = 255, Max = 255})
    SettingsTab:AddSlider({Name = "Green", Flag = "FovGreen", Default = 255, Max = 255})
    SettingsTab:AddSlider({Name = "Blue", Flag = "FovBlue", Default = 255, Max = 255})
    SettingsTab:AddSlider({Name = "Smoothness", Flag = "Smoothing", Min = 12, Default = 40, Max = 75})
end

print("Fu Kang Hub noob fps รันเเล้ว Siuu")
end)

local Section = Tab:NewSection("RoBeats")

Section:NewToggle("RoBeats (Auto Play)", "Fu Kang", function(state)
    if state then
        print("Toggle On")
        loadstring(game:HttpGet("https://raw.githubusercontent.com/FujiXDDDDDDDDD1/RB/main/README.md"))()
        print("Toggle Off")
    end
end)

local Section = Tab:NewSection("Funky Friday")

Section:NewButton("Funky Friday Hack", "Fu Kang Hub", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/wally-rblx/funky-friday-autoplay/main/main.lua",true))()
end)

local Section = Tab:NewSection("Combat Warriors")

Section:NewButton("Combat Warriors Hack", "Fu Kang Hub", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/SussyImposterRed/Scripts/main/NOVA_HUB_SOURCE"))()
end)

local Section = Tab:NewSection("Expedition Antarctica")

Section:NewButton("Expedition Antarctica Hack", "Morfin's Mods", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/SirMorfin/Morfins-Mods/main/Expedition%20Antarctica"))()
end)

local Section = Tab:NewSection("BedWars")

Section:NewButton("BedWars Hack", "Fu Kang hub", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/FujiXDDDDDDDDD1/BW/main/README.md"))()
end)

local Section = Tab:NewSection("Build A Boat For Treasure")

Section:NewButton("Build A Boat For Treasure Hack", "Vynixu Hub", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Vynixius/main/Build%20A%20Boat%20For%20Treasure/Script.lua"))()
end)

local Section = Tab:NewSection("Vehicle Legends")

Section:NewButton("Vehicle Legends Hack", "Wheel Hub", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/AaronS69420/WheelHub/main/MainFile", true))()
end)

Section:NewButton("Key gfhdyhtrsytrstrsgfsyf", "Fu Kang Hub V2", function()
    print("gfhdyhtrsytrstrsgfsyf")
end)

local Section = Tab:NewSection("Driving Empire")

Section:NewButton("Driving Empire Hack", "Wheel Hub", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/AaronS69420/WheelHub/main/MainFile", true))()
end)

Section:NewButton("Key gfhdyhtrsytrstrsgfsyf", "Fu Kang Hub V2", function()
    print("gfhdyhtrsytrstrsgfsyf")
end)

local Section = Tab:NewSection("Evade")

Section:NewButton("Evade Hack", "Fu Kang Hub V2", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/FujiXDDDDDDDDD1/Evade.lua/main/README.md"))()
end)

local Tab = Window:NewTab("Other")
local Section = Tab:NewSection("Natural Disaster Survival")

Section:NewButton("Natural Disaster Survival Teleport 1", "Fu Kang Hub", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-284.619812, 194.09996, 326.953094, 0.452830076, -8.86669866e-08, -0.891596854, 3.79251155e-08, 1, -8.01857354e-08, 0.891596854, 2.49660137e-09, 0.452830076)
end)

Section:NewButton("Natural Disaster Survival Teleport 2", "Fu Kang Hub", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-79.550827, 47.4999924, -0.644881904, 0.16489394, -1.1451017e-08, -0.986311316, 1.06218234e-08, 1, -9.83415926e-09, 0.986311316, -8.85483153e-09, 0.16489394)
end)

local Section = Tab:NewSection("City BanNa")

Section:NewButton("Farm 1", "Fu Kang Hub", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-358.350952, 92.1009369, 529.487305, -0.0714133084, -4.09426661e-08, -0.997446835, -7.905156e-08, 1, -3.53876857e-08, 0.997446835, 7.63225714e-08, -0.0714133084)
end)

Section:NewButton("Farm 2", "Fu Kang Hub", function()
    local TweenService = game:GetService("TweenService")
local Tw = TweenService:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(20, Enum.EasingStyle.Linear, Enum.EasingDirection.Out,0,false,0), 
{CFrame = CFrame.new(448.92688, 62.6451378, 336.904694, -0.954144955, -7.07577419e-09, -0.299344987, -1.96142186e-10, 1, -2.30123316e-08, 0.299344987, -2.18983853e-08, -0.954144955)}):Play()
end)

local Tab = Window:NewTab("Settings")
local Section = Tab:NewSection("Hide UI")

Section:NewKeybind("Hide UI", "Fu Kang Hub", Enum.KeyCode.RightShift, function()
	Library:ToggleUI()
end)

print("Script Fu Kang Hub V2 รันเเล้ว Siuu")
