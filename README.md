local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/zxciaz/VenyxUI/main/Reuploaded"))() --someone reuploaded it so I put it in place of the original back up so guy can get free credit.
local venyx = library.new("Test1", 5013109572)
    local page = venyx:addPage("LocalTest", 5012544693)
    local section1 = page:addSection("Page1")
    
    section1:addToggle("AutoFully", nil, function(a)
 _G.Auto = a
 while _G.Auto do wait(1)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(178.605743, 305.841187, -352.844421, 0.152919233, -7.10493619e-09, -0.988238692, 4.58264671e-09, 1, -6.4803789e-09, 0.988238692, -3.5377743e-09, 0.152919233)
        wait(.5)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(84.552803, 721.868591, -124.128059, -0.707051098, 3.78424652e-08, -0.70716244, 1.25479867e-12, 1, 5.35118581e-08, 0.70716244, 3.78347309e-08, -0.707051098)
        wait(1)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(207.399612, 713.799805, -185.042465, -0.197074741, -7.75883535e-08, -0.980388463, 3.91774346e-09, 1, -7.99279505e-08, 0.980388463, -1.95926901e-08, -0.197074741)
        wait(1)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(350.93512, 796.799805, -181.944595, 0.0739125833, 3.01274845e-08, -0.997264743, 1.80521447e-08, 1, 3.15480584e-08, 0.997264743, -2.03345643e-08, 0.0739125833)
        wait()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(385.862518, 797.749817, -131.588303, -0.995132923, -4.03044851e-08, 0.098541908, -4.00858085e-08, 1, 4.19903445e-09, -0.098541908, 2.28465608e-10, -0.995132923)
        game:GetService("ReplicatedStorage"):WaitForChild("Honeypot"):WaitForChild("Internal"):WaitForChild("RemoteStorage"):WaitForChild("Rebirth - RemoteEvent"):FireServer()
 end
    end)
    section1:addButton("infiniteyield", function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
    end)
    section1:addKeybind("Toggle Keybind", Enum.KeyCode.M, function()
        print("Activated Keybind")
        venyx:toggle()
        end, function()
        print("Changed Keybind")
        end)
    section1:addSlider("WalkSpeed", 16, -100, 400, function(value)
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = value
        end)
    section1:addSlider("JumpPower", 42, -100, 400, function(value)
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = value
        end)


--theme page
local themes = {
    Background = Color3.fromRGB(129, 91, 91),
    Glow = Color3.fromRGB(235, 101, 101),
    Accent = Color3.fromRGB(189, 119, 119),
    LightContrast = Color3.fromRGB(87, 49, 49),
    DarkContrast = Color3.fromRGB(121, 67, 67),  
    TextColor = Color3.fromRGB(255, 255, 255)
    }
    local theme = venyx:addPage("Theme(Bug)", 5012544693)
    local colors = theme:addSection("Colors")
    
    for theme, color in pairs(themes) do -- all in one theme changer, i know, im cool
    colors:addColorPicker(theme, color, function(color3)
    venyx:setTheme(theme, color3)
    end)
    end 
    venyx:SelectPage(venyx.pages[1], true) -- no default for more freedom
