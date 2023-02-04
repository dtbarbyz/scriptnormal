-- Ссылка на Библиотеку
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Robojini/Tuturial_UI_Library/main/UI_Template_1"))()
--[[ 
В данный момент стоит тема "RJTheme3" ,
вы можете использовать другую тему приведённую ниже -
"RJTheme1"
"RJTheme2"
"RJTheme3"ц
"RJTheme4"
"RJTheme5"
"RJTheme6"
"RJTheme7"
"RJTheme8"
//////////////////////////////////////////////////////////////////

Что бы сделать свою тему , уберите часть скрипта из "комминтариев" ,
который находится чуть ниже , и вместо "RJTheme3" в переменной "Windows" - 
напишите переменную которая используется в скрипте чуть ниже .
]]
--[[
local colors = {
    -- Цвет фона у Секций
    SchemeColor = Color3.fromRGB(150, 72, 148),
    -- Цвет фона в правой части UI
    Background = Color3.fromRGB(15,15,15),
    -- Цвет фона в левой части UI
 Header = Color3.fromRGB(15,15,15),
    -- Цвет текста
    TextColor = Color3.fromRGB(255,255,255),
    -- Цвет фона у кнопок
    ElementColor = Color3.fromRGB(20, 20, 20)
}
]]
-- Создать окно UI
local Window = Library.CreateLib("Arbyz karapyz Hub", "RJTheme3")

-- Секция
local Tab = Window:NewTab("Player")
local Tab2 = Window:NewTab("Teleport")

-- Подсекция
local Section = Tab:NewSection("xd")
local Section2 = Tab2:NewSection("xd2")

Section:NewLabel("Player")

Section:NewButton("WalkSpeed", "ButtonInfo", function()
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 100
end)


Section:NewButton("JumpPower", "ButtonInfo", function()
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = 100

end)


Section:NewButton("Headless", "ButtonInfo", function()
    game.Players.LocalPlayer.Character.Head.Transparency = 1
    game.Players.LocalPlayer.Character.Head.face:Remove ()
end)


Section:NewButton("AntiRagdoll", "ButtonInfo", function()
    game.Players.LocalPlayer.Character.Pushed:Remove ()
    game.Players.LocalPlayer.Character.RagdollMe:Remove ()
end)