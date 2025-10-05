-- Toggle com nome do usuário e notificação de Discord

local Players = game:GetService("Players")
local StarterGui = game:GetService("StarterGui")

local function showNotification()
    StarterGui:SetCore("SendNotification", {
        Title = "@Yay Cat",
        Text = "Entre no meu Discord: discord.gg/SYEz83rKR4",
        Duration = 10
    })
end

-- Cria um toggle fictício (não clicável) na tela
local player = Players.LocalPlayer
local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Name = "YayCatToggleGui"
ScreenGui.Parent = player:WaitForChild("PlayerGui")

local ToggleFrame = Instance.new("Frame")
ToggleFrame.Size = UDim2.new(0, 200, 0, 50)
ToggleFrame.Position = UDim2.new(0.5, -100, 0.1, 0)
ToggleFrame.BackgroundColor3 = Color3.fromRGB(35, 40, 50)
ToggleFrame.Parent = ScreenGui

local NameLabel = Instance.new("TextLabel")
NameLabel.Size = UDim2.new(1, 0, 1, 0)
NameLabel.Position = UDim2.new(0, 0, 0, 0)
NameLabel.BackgroundTransparency = 1
NameLabel.Text = "@Yay Cat"
NameLabel.Font = Enum.Font.SourceSansBold
NameLabel.TextSize = 24
NameLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
NameLabel.Parent = ToggleFrame

-- Notifica ao entrar
showNotification()
