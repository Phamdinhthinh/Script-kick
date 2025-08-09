-- BOST GUI Script - by bạn
-- Menu hack cho game của bạn

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Tạo ScreenGui
local gui = Instance.new("ScreenGui")
gui.Parent = game.CoreGui

-- Frame chính
local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 250, 0, 300)
frame.Position = UDim2.new(0.1, 0, 0.1, 0)
frame.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
frame.Parent = gui

-- Tiêu đề
local title = Instance.new("TextLabel")
title.Text = "BOST Hack Menu"
title.Size = UDim2.new(1, 0, 0, 40)
title.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
title.TextColor3 = Color3.fromRGB(255, 255, 255)
title.Parent = frame

-- Hàm tạo nút
local function createButton(text, yPos, callback)
    local btn = Instance.new("TextButton")
    btn.Text = text
    btn.Size = UDim2.new(1, -20, 0, 30)
    btn.Position = UDim2.new(0, 10, 0, yPos)
    btn.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
    btn.TextColor3 = Color3.fromRGB(255, 255, 255)
    btn.Parent = frame
    btn.MouseButton1Click:Connect(callback)
end

-- Nút tăng speed
createButton("Speed 100", 50, function()
    if character:FindFirstChild("Humanoid") then
        character.Humanoid.WalkSpeed = 100
    end
end)

-- Nút tăng jump
createButton("Jump 150", 90, function()
    if character:FindFirstChild("Humanoid") then
        character.Humanoid.JumpPower = 150
    end
end)

-- Nút Fly
createButton("Fly Mode", 130, function()
    loadstring(game:HttpGet("https://pastebin.com/raw/6d9H1sGJ"))() -- link fly (VD)
end)

-- Nút Teleport đến Spawn
createButton("TP to Spawn", 170, function()
    if workspace:FindFirstChild("SpawnLocation") then
        character:MoveTo(workspace.SpawnLocation.Position + Vector3.new(0, 5, 0))
    end
end)

-- Nút reset GUI
createButton("Reset Character", 210, function()
    character:BreakJoints()
end)
