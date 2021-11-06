if game:GetService("CoreGui"):FindFirstChild("FluxLib") then
    game:GetService("CoreGui").FluxLib:Destroy()
end

local Flux = loadstring(game:HttpGet"https://raw.githubusercontent.com/dawid-scripts/UI-Libs/main/fluxlib.txt")()

local win = Flux:Window("PREVIEW", "Baseplate", Color3.fromRGB(255, 110, 48), Enum.KeyCode.RightControl)
local tab = win:Tab("Tab 1", "http://www.roblox.com/asset/?id=6023426915")


function EquipWeapon(ToolSe)
    if game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe) then
       local tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
       wait()
       game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
    end
 end


Weapon = {}
for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do  
    if v:IsA("Tool") then
        table.insert(Weapon ,v.Name)
    end
end

for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do  
    if v:IsA("Tool") then
        table.insert(Weapon ,v.Name)
    end
end


local SelectWeapon = tab:Dropdown("Select Weapon",Weapon,function(Value)
    SelectToolWeapon = Value
end)

tab:Button("Refresh Weapon"," ",function()
    SelectWeapon:Clear()
    Weapon = {}
    for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do  
        if v:IsA("Tool") then
            SelectWeapon:Add(v.Name)
        end
    end
    for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do  
        if v:IsA("Tool") then
            SelectWeapon:Add(v.Name)
        end
    end
end)


tab:Toggle("Auto Farm","fafafa",false,function(t)
autofarm = t
end)

game:GetService("RunService").Heartbeat:Connect(function()
    if autofarm then
     pcall(function()
       game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
     end)
    end
 end)

 function Quest()
	MyLevel = game:GetService("Players").LocalPlayer.Data.Level.Value
    if MyLevel == 1 or MyLevel <= 9 then
        Mon = "Bandit [Lv. 5]"
        LevelQuest = 1
        NameQuest = "BanditQuest1"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(1060.3233642578, 16.36280632019, 1549.2186279297)

    elseif MyLevel == 10 or MyLevel <= 14 then
        Mon = "Monkey [Lv. 14]"
        LevelQuest = 1
        NameQuest = "JungleQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838, 0, 0, 1, 0, 1, -0, -1, 0, 0)
    
    elseif MyLevel == 15 or MyLevel <= 29 then
        Mon = "Gorilla [Lv. 20]"
        LevelQuest = 2
        NameQuest = "JungleQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838, 0, 0, 1, 0, 1, -0, -1, 0, 0)
    
    elseif MyLevel == 30 or MyLevel <= 39 then
        Mon = "Pirate [Lv. 35]"
        LevelQuest = 1
        NameQuest = "BuggyQuest1"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(-1141.07483, 4.10001802, 3831.5498, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
    
    elseif MyLevel == 40 or MyLevel <= 59 then
        Mon = "Brute [Lv. 45]"
        LevelQuest = 2
        NameQuest = "BuggyQuest1"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(-1141.07483, 4.10001802, 3831.5498, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
    
    elseif MyLevel == 60 or MyLevel <= 74 then
        Mon = "Desert Bandit [Lv. 60]"
        LevelQuest = 1
        NameQuest = "DesertQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(894.488647, 5.14000702, 4392.43359, 0.819155693, -0, -0.573571265, 0, 1, -0, 0.573571265, 0, 0.819155693)
    
    elseif MyLevel == 75 or MyLevel <= 89 then
        Mon = "Desert Officer [Lv. 70]"
        LevelQuest = 2
        NameQuest = "DesertQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(894.488647, 5.14000702, 4392.43359, 0.819155693, -0, -0.573571265, 0, 1, -0, 0.573571265, 0, 0.819155693)
    
    elseif MyLevel == 90 or MyLevel <= 99 then
        Mon = "Snow Bandit [Lv. 90]"
        LevelQuest = 1
        NameQuest = "SnowQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(1389.74451, 88.1519318, -1298.90796, -0.342042685, 0, 0.939684391, 0, 1, 0, -0.939684391, 0, -0.342042685)
    
    elseif MyLevel == 100 or MyLevel <= 119 then
        Mon = "Snowman [Lv. 100]"
        LevelQuest = 2
        NameQuest = "SnowQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(1389.74451, 88.1519318, -1298.90796, -0.342042685, 0, 0.939684391, 0, 1, 0, -0.939684391, 0, -0.342042685)
    
    elseif MyLevel == 120 or MyLevel <= 149 then
        Mon = "Chief Petty Officer [Lv. 120]"
        LevelQuest = 1
        NameQuest = "MarineQuest2"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(-5039.58643, 27.3500385, 4324.68018, 0, 0, -1, 0, 1, 0, 1, 0, 0)
    
    elseif MyLevel == 150 or MyLevel <= 174 then
        Mon = "Sky Bandit [Lv. 150]"
        LevelQuest = 1
        NameQuest = "SkyQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(-4839.53027, 716.368591, -2619.44165, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
    
    elseif MyLevel == 175 or MyLevel <= 224 then
        Mon = "Dark Master [Lv. 175]"
        LevelQuest = 2
        NameQuest = "SkyQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(-4839.53027, 716.368591, -2619.44165, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
    
    elseif MyLevel == 225 or MyLevel <= 274 then
        Mon = "Toga Warrior [Lv. 225]"
        LevelQuest = 1
        NameQuest = "ColosseumQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(-1580.04663, 6.35000277, -2986.47534, -0.515037298, 0, -0.857167721, 0, 1, 0, 0.857167721, 0, -0.515037298)
    
    elseif MyLevel == 275 or MyLevel <= 299 then
        Mon = "Gladiator [Lv. 275]"
        LevelQuest = 2
        NameQuest = "ColosseumQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(-1580.04663, 6.35000277, -2986.47534, -0.515037298, 0, -0.857167721, 0, 1, 0, 0.857167721, 0, -0.515037298)
    
    elseif MyLevel == 300 or MyLevel <= 329 then
        Mon = "Military Soldier [Lv. 300]"
        LevelQuest = 1
        NameQuest = "MagmaQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(-5313.37012, 10.9500084, 8515.29395, -0.499959469, 0, 0.866048813, 0, 1, 0, -0.866048813, 0, -0.499959469)
    
    elseif MyLevel == 330 or MyLevel <= 374 then
        Mon = "Military Spy [Lv. 330]"
        LevelQuest = 2
        NameQuest = "MagmaQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(-5313.37012, 10.9500084, 8515.29395, -0.499959469, 0, 0.866048813, 0, 1, 0, -0.866048813, 0, -0.499959469)
    
    elseif MyLevel == 375 or MyLevel <= 399 then
        Mon = "Fishman Warrior [Lv. 375]"
        LevelQuest = 1
        NameQuest = "FishmanQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(61121.1094, 17.953125, 1564.52637, -0.913477898, 0, -0.406888306, 0, 1, 0, 0.406888306, 0, -0.913477898)
    
    elseif MyLevel == 400 or MyLevel <= 449 then
        Mon = "Fishman Commando [Lv. 400]"
        LevelQuest = 2
        NameQuest = "FishmanQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(61121.1094, 17.953125, 1564.52637, -0.913477898, 0, -0.406888306, 0, 1, 0, 0.406888306, 0, -0.913477898)
    
    elseif MyLevel == 450 or MyLevel <= 474 then
        Mon = "God's Guard [Lv. 450]"
        LevelQuest = 1
        NameQuest = "SkyExp1Quest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(-4721.88867, 843.874695, -1949.96643, 0.996191859, -0, -0.0871884301, 0, 1, -0, 0.0871884301, 0, 0.996191859)
    
    elseif MyLevel == 475 or MyLevel <= 524 then
        Mon = "Shanda [Lv. 475]"
        LevelQuest = 2
        NameQuest = "SkyExp1Quest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(-7859.09814, 5544.19043, -381.476196, -0.422592998, 0, 0.906319618, 0, 1, 0, -0.906319618, 0, -0.422592998)
    
    elseif MyLevel == 525 or MyLevel <= 549 then
        Mon = "Royal Squad [Lv. 525]"
        LevelQuest = 1
        NameQuest = "SkyExp2Quest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(-7906.81592, 5634.6626, -1411.99194, 0, 0, -1, 0, 1, 0, 1, 0, 0)
    
    elseif MyLevel == 550 or MyLevel <= 624 then
        Mon = "Royal Soldier [Lv. 550]"
        LevelQuest = 2
        NameQuest = "SkyExp2Quest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(-7906.81592, 5634.6626, -1411.99194, 0, 0, -1, 0, 1, 0, 1, 0, 0)
    
    elseif MyLevel == 625 or MyLevel <= 649 then
        Mon = "Galley Pirate [Lv. 625]"
        LevelQuest = 1
        NameQuest = "FountainQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(5259.81982, 37.3500175, 4050.0293, 0.087131381, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, 0.087131381)
    
    elseif MyLevel == 650 or MyLevel <= 700 then
        Mon = "Galley Captain [Lv. 650]"
        LevelQuest = 2
        NameQuest = "FountainQuest"
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(5259.81982, 37.3500175, 4050.0293, 0.087131381, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, 0.087131381)
    end
end

spawn(function()
    while wait() do
        if autofarm then
			pcall(function()
    if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
		Quest()
	game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameQuest
    wait(1.1) 
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest" , NameQuest , LevelQuest) 
    elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
		Quest()
        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
        if v.Name == Mon then
			game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
            repeat wait(.1)
				if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) then
                pcall(function()
                    EquipWeapon(SelectToolWeapon)
                end)
                if sethiddenproperty then 
                    sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                end
				game:GetService('VirtualUser'):CaptureController()
				game:GetService('VirtualUser'):ClickButton1(Vector2.new(999, 999), game:GetService("Workspace").Camera.CFrame)
            v.HumanoidRootPart.Size = Vector3.new(50,50,50)
            v.HumanoidRootPart.CanCollide = false
            v.Humanoid:ChangeState(11)
            game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 0)
            Magnet = true
            MobMagnet = v.HumanoidRootPart.CFrame 
			else
				Magnet = false
				Quest()
				game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameQuest
				wait(1.1) 
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest" , NameQuest , LevelQuest) 
			end
            until v.Humanoid.Health <= 0 or autofarm == false or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
            Magnet = false
            if autofarm == false then return end
		else
			game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
        end
    
    end
    
    end
end)
    end
    end
    end)

    
spawn(function()
    while wait(.2) do
        if Magnet then
			pcall(function()
            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                if v.Name == Mon then
                    v.HumanoidRootPart.CFrame = MobMagnet
                    v.Humanoid:ChangeState(14)
					v.HumanoidRootPart.Size = Vector3.new(50,50,50)
					v.HumanoidRootPart.CanCollide = false
					v.Humanoid:ChangeState(11)
                end
            end
		end)
        end
    end
end)
