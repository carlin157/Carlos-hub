local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()

local Window = Fluent:CreateWindow({
    Title = "Carlos hub",
    Size = UDim2.fromOffset(400, 300),
    Theme = "Light"
})

local MainTab = Window:AddTab({ Title = "Principal" })

AdminsSection:NewButton("Infinite Yield", nil, function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
end)

local Slider = MainTab:AddSlider("Volume", {
    Title = "Ajuste o Volume",
    Min = 0, Max = 100, Default = 50
})

Slider:OnChanged(function(Value)
    print("Volume ajustado para:", Value)
end)

Fluent:Notify({
    Title = "Bem-vindo",
    Content = "Interface carregada com sucesso!"
})
