local player = game.Players.LocalPlayer
local gui = Instance.new("ScreenGui", player:WaitForChild("PlayerGui"))
gui.Name = "HunterUI"

-- Main frame (cả bảng UI)
local mainFrame = Instance.new("Frame", gui)
mainFrame.Size = UDim2.new(0, 600, 0, 350)
mainFrame.Position = UDim2.new(0.5, -300, 0.5, -175)
mainFrame.BackgroundColor3 = Color3.fromRGB(25, 25, 25)

Instance.new("UICorner", mainFrame).CornerRadius = UDim.new(0, 10)

-- Sidebar
local sidebar = Instance.new("Frame", mainFrame)
sidebar.Size = UDim2.new(0, 150, 1, 0)
sidebar.Position = UDim2.new(0, 0, 0, 0)
sidebar.BackgroundColor3 = Color3.fromRGB(40, 40, 40)

-- Danh sách tab bên sidebar
local tabNames = {"Main", "Premium", "Emergency", "Settings"}

for i, name in ipairs(tabNames) do
	local tabButton = Instance.new("TextButton", sidebar)
	tabButton.Size = UDim2.new(1, -20, 0, 40)
	tabButton.Position = UDim2.new(0, 10, 0, (i - 1) * 45 + 10)
	tabButton.Text = name
	tabButton.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
	tabButton.TextColor3 = Color3.fromRGB(255, 255, 255)
	Instance.new("UICorner", tabButton).CornerRadius = UDim.new(0, 6)
end

-- Nội dung tab Main
local contentFrame = Instance.new("Frame", mainFrame)
contentFrame.Size = UDim2.new(1, -160, 1, -20)
contentFrame.Position = UDim2.new(0, 160, 0, 10)
contentFrame.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
Instance.new("UICorner", contentFrame).CornerRadius = UDim.new(0, 6)

-- Label Main
local title = Instance.new("TextLabel", contentFrame)
title.Size = UDim2.new(1, 0, 0, 30)
title.Position = UDim2.new(0, 0, 0, 0)
title.Text = "Main"
title.TextColor3 = Color3.fromRGB(255, 255, 255)
title.BackgroundTransparency = 1
title.Font = Enum.Font.SourceSansBold
title.TextSize = 22

-- Dropdown giả (Select Dungeon)
local dungeonDrop = Instance.new("TextBox", contentFrame)
dungeonDrop.Size = UDim2.new(0, 200, 0, 30)
dungeonDrop.Position = UDim2.new(0, 20, 0, 50)
dungeonDrop.Text = "Select Dungeon"
dungeonDrop.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
dungeonDrop.TextColor3 = Color3.fromRGB(255, 255, 255)

-- Dropdown giả (Difficulty)
local difficultyDrop = Instance.new("TextBox", contentFrame)
difficultyDrop.Size = UDim2.new(0, 200, 0, 30)
difficultyDrop.Position = UDim2.new(0, 20, 0, 90)
difficultyDrop.Text = "Select Difficulty"
difficultyDrop.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
difficultyDrop.TextColor3 = Color3.fromRGB(255, 255, 255)

-- Toggle button generator
local toggles = {
	{"Auto Farm", 130},
	{"Auto Join Dungeon", 170},
	{"Auto Leave Dungeon", 210},
	{"Auto Reawaken", 250},
}

for _, data in ipairs(toggles) do
	local label = Instance.new("TextLabel", contentFrame)
	label.Size = UDim2.new(0, 160, 0, 30)
	label.Position = UDim2.new(0, 20, 0, data[2])
	label.Text = data[1]
	label.BackgroundTransparency = 1
	label.TextColor3 = Color3.fromRGB(255, 255, 255)

	local toggle = Instance.new("TextButton", contentFrame)
	toggle.Size = UDim2.new(0, 50, 0, 25)
	toggle.Position = UDim2.new(0, 200, 0, data[2])
	toggle.Text = "OFF"
	toggle.BackgroundColor3 = Color3.fromRGB(100, 0, 0)
	toggle.TextColor3 = Color3.fromRGB(255, 255, 255)

	toggle.MouseButton1Click:Connect(function()
		if toggle.Text == "OFF" then
			toggle.Text = "ON"
			toggle.BackgroundColor3 = Color3.fromRGB(0, 150, 0)
		else
			toggle.Text = "OFF"
			toggle.BackgroundColor3 = Color3.fromRGB(100, 0, 0)
		end
	end)
end
