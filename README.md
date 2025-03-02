local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer

-- Criando a GUI
local screenGui = Instance.new("ScreenGui")
screenGui.Parent = LocalPlayer:WaitForChild("PlayerGui")

local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 300, 0, 200)
frame.Position = UDim2.new(0.5, -150, 0.5, -100)
frame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
frame.BackgroundTransparency = 0.3
frame.Parent = screenGui

local titleLabel = Instance.new("TextLabel")
titleLabel.Size = UDim2.new(1, 0, 0, 30)
titleLabel.Text = "💀 Brookhaven Exploit v1.0 💀"
titleLabel.TextColor3 = Color3.fromRGB(0, 255, 0)
titleLabel.BackgroundTransparency = 1
titleLabel.TextScaled = true
titleLabel.Parent = frame

local messageLabel = Instance.new("TextLabel")
messageLabel.Size = UDim2.new(1, -20, 0, 100)
messageLabel.Position = UDim2.new(0, 10, 0, 40)
messageLabel.Text = "Injecting...\nBypassing Anti-Cheat...\nAccessing Admin Panel..."
messageLabel.TextColor3 = Color3.fromRGB(0, 255, 0)
messageLabel.BackgroundTransparency = 1
messageLabel.TextXAlignment = Enum.TextXAlignment.Left
messageLabel.TextYAlignment = Enum.TextYAlignment.Top
messageLabel.TextScaled = false
messageLabel.Font = Enum.Font.Code
messageLabel.Parent = frame

local hackButton = Instance.new("TextButton")
hackButton.Size = UDim2.new(0.8, 0, 0, 40)
hackButton.Position = UDim2.new(0.1, 0, 0.7, 0)
hackButton.Text = "ENABLE GOD MODE ⚠️"
hackButton.TextScaled = true
hackButton.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
hackButton.TextColor3 = Color3.fromRGB(255, 255, 255)
hackButton.Parent = frame

-- Efeito de texto piscando
spawn(function()
    while true do
        messageLabel.Text = "Injecting...\nBypassing Anti-Cheat...\nAccessing Admin Panel..."
        wait(1)
        messageLabel.Text = "Injecting...\nBypassing Anti-Cheat...\nERROR: Connection Lost."
        wait(1)
    end
end)

-- Mensagem de troll ao clicar no botão
hackButton.MouseButton1Click:Connect(function()
    hackButton.Text = "ERROR: DETECTED ❌"
    wait(1)
    hackButton.Text = "BANNED FROM BROOKHAVEN 🚨"
    wait(3)
    
    -- Expulsar o jogador do jogo
    LocalPlayer:Kick("⚠️ Você foi banido do Brookhaven! Contate o suporte para mais informações.")
end)
