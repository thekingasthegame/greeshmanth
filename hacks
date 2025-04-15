local Window = Rayfield:CreateWindow({
   Name = "Simple Blox Fruits Hub (Keyless)",
   LoadingTitle = "Blox Fruits Hub",
   LoadingSubtitle = "by ChatGPT",
   ConfigurationSaving = {
      Enabled = false
   },
   Discord = {
      Enabled = false
   },
   KeySystem = false
})

-- Autofarm Section
local AutoFarmTab = Window:CreateTab("🏝️ Auto Farm", 4483362458)
local AutoFarmToggle = AutoFarmTab:CreateToggle({
    Name = "Auto Farm Enemies",
    CurrentValue = false,
    Callback = function(Value)
        getgenv().AutoFarm = Value
        while getgenv().AutoFarm do
            pcall(function()
                local Enemy = workspace.Enemies:FindFirstChildOfClass("Model")
                if Enemy and Enemy:FindFirstChild("HumanoidRootPart") then
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Enemy.HumanoidRootPart.CFrame * CFrame.new(0, 10, 0)
                    game:GetService("VirtualInputManager"):SendKeyEvent(true, "Z", false, game)
                end
            end)
            task.wait(1)
        end
    end,
})

-- Teleport Section
local TeleportTab = Window:CreateTab("📍 Teleports", 4483362458)
TeleportTab:CreateButton({
    Name = "Teleport to Jungle Island",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1615, 35, 145)
    end,
})
TeleportTab:CreateButton({
    Name = "Teleport to Marine Fortress",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-450
