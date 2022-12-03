local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
	local Window = Library.CreateLib("Snitch Town By trsiL_", "DarkTheme")
	local Tab = Window:NewTab("main")
	local Section = Tab:NewSection("No Cooldown")
	Section:NewToggle("No Cooldown", "ไว้ใช้ที่มีกดตัว E จะได้ไม่ต้องรอ", function(Wood)
		while wait(2) do
			for i,v in pairs(workspace:GetDescendants()) do
				if v:IsA("ProximityPrompt") then
					if v.Enabled == false then
						v.Enabled = true
					end
					if v.HoldDuration ~= 0 then
						v.HoldDuration = 0
					end
				end
			end
		end
	end)
	
local Section = Tab:NewSection("On Cooldown")
	Section:NewToggle("On Cooldown", "ให้กลับมาเป็นค่าเดิม", function(Wood)
		while wait(2) do
			for i,v in pairs(workspace:GetDescendants()) do
				if v:IsA("ProximityPrompt") then
					if v.Enabled == false then
						v.Enabled = true
					end
					if v.HoldDuration ~= 3 then
						v.HoldDuration = 3
					end
				end
			end
		end
	end)

local Tab = Window:NewTab("TP")
	local Section = Tab:NewSection("TP")
	Section:NewToggle("Teleport Label Red", "วาปไป Label ระวังคนเห็น!", function(Wood)
		game.Players.localPlayer.character.HumanoidRootPart.CFrame = CFrame.new(-3765.51318, 282.389099, 2585.78223, -0.00415584585, 7.57563114e-08, -0.999991357, 2.19104788e-08, 1, 7.56659091e-08, 0.999991357, -2.15958345e-08, -0.00415584585)
	end)
	Section:NewToggle("Teleport Mine","วาปไป Mine ระวังคนเห็น!", function(Wood)
		game.Players.localPlayer.character.HumanoidRootPart.CFrame = CFrame.new(71.4835815, 353.435181, -1427.70923, 0.415955067, -2.65472044e-09, -0.909385145, -8.20917201e-09, 1, -6.67414346e-09, 0.909385145, 1.02414432e-08, 0.415955067)
	end)
	Section:NewToggle("Teleport Farm", "วาปไป Farm ระวังคนเห็น!", function(Wood)
		game.Players.localPlayer.character.HumanoidRootPart.CFrame = CFrame.new(-1971.30115, 281.984283, -1139.34985, -0.317340285, -1.03927933e-08, -0.948311746, 3.03945527e-08, 1, -2.11304041e-08, 0.948311746, -3.5529041e-08, -0.317340285)
	end)
	Section:NewToggle("Teleport Label Blue", "วาปไป Label Blue ระวังคนเห็น!", function(Wood)
		game.Players.localPlayer.character.HumanoidRootPart.CFrame = CFrame.new(-901.661865234375, 382.6925048828125, 6046.515625)
	end)
		Section:NewToggle("Teleport Cement1", "วาปไปจกปูน1 ระวังคนเห็น!", function(Wood)
		game.Players.localPlayer.character.HumanoidRootPart.CFrame = CFrame.new(-904.973388671875, 282.1530456542969, 4431.97705078125)
		end)
	Section:NewToggle("Teleport Cement2", "วาปไปจกปูน2 ระวังคนเห็น!", function(Wood)
		game.Players.localPlayer.character.HumanoidRootPart.CFrame = CFrame.new(-904.973388671875, 282.1530456542969, 4431.97705078125)
	end)
		Section:NewToggle("Teleport Cement3", "วาปไปจกปูน3 ระวังคนเห็น!", function(Wood)
		game.Players.localPlayer.character.HumanoidRootPart.CFrame = CFrame.new(-1922.75390625, 339.32684326171875, 3628.8203125)
	end)
	Section:NewToggle("Teleport Wood", "วาปไป Wood ระวังแอดมินจับได้! ตัดแล้วรีบขาย!", function(Wood)
		game.Players.localPlayer.character.HumanoidRootPart.CFrame = CFrame.new(-492.8077697753906, 385.5323486328125, -1726.140625)
		wait(0.1)
		local Noclip = Instance.new("Part",workspace)
		Noclip.Name = "Noclip"
		Noclip.CanCollide = true
		Noclip.Anchored = true
		Noclip.Transparency = 0 
		Noclip.Size = Vector3.new(30,5,30)
		Noclip.Position = Vector3.new(-492.8077697753906, 380.5323486328125, -1726.140625)
	end)
	
local Tab = Window:NewTab("HitBox")
	local Section = Tab:NewSection("HitBoxView")
		Section:NewToggle("HitBoxView", "ให้ดูระยะในการตี", function(HitBoxView)
	_G.HeadSize = 10
_G.Disabled = true

game:GetService('RunService').RenderStepped:connect(function()
if _G.Disabled then
for i,v in next, game:GetService('Players'):GetPlayers() do
if v.Name ~= game:GetService('Players').LocalPlayer.Name then
pcall(function()
v.Character.HumanoidRootPart.Size = Vector3.new(_G.HeadSize,_G.HeadSize,_G.HeadSize)
v.Character.HumanoidRootPart.Transparency = 0.9
v.Character.HumanoidRootPart.BrickColor = BrickColor.new("Really red")
v.Character.HumanoidRootPart.Material = "Neon"
v.Character.HumanoidRootPart.CanCollide = false
end)
end
end
end
end)
end)

local Section = Tab:NewSection("HitBoxNotView")
		Section:NewToggle("HitBoxNotView", "แชร์จอเล่นได้ให้หลอกพวกโง่", function(HitBoxView)
	_G.HeadSize = 10
_G.Disabled = true

game:GetService('RunService').RenderStepped:connect(function()
if _G.Disabled then
for i,v in next, game:GetService('Players'):GetPlayers() do
if v.Name ~= game:GetService('Players').LocalPlayer.Name then
pcall(function()
v.Character.HumanoidRootPart.Size = Vector3.new(_G.HeadSize,_G.HeadSize,_G.HeadSize)
v.Character.HumanoidRootPart.Transparency = 1
v.Character.HumanoidRootPart.BrickColor = BrickColor.new("Really red")
v.Character.HumanoidRootPart.Material = "Neon"
v.Character.HumanoidRootPart.CanCollide = false
end)
end
end
end
end)
end)
