--- made by wiwat007zyx
local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("ImageLabel")
local TextLabel = Instance.new("TextLabel")

--Properties:

ScreenGui.Parent = game:GetService("CoreGui")

Frame.Name = "Frame"
Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.new(1.000000, 1.000000, 1.000000)
Frame.BackgroundTransparency = 0.000
Frame.Position = UDim2.new(-0.254758418, 0, -0.37299037, 0)
Frame.Size = UDim2.new(110, 2061, 110, 1048)
Frame.Image = "rbxassetid://3570695787"
Frame.ImageColor3 = Color3.new(1.000000, 1.000000, 1.000000)
Frame.ScaleType = Enum.ScaleType.Slice
Frame.SliceCenter = Rect.new(100, 100, 100, 100)
Frame.SliceScale = 0.120

TextLabel.Parent = ScreenGui
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.Position = UDim2.new(0.419472903, 0, 0.443729907, 0)
TextLabel.Size = UDim2.new(0, 219, 0, 70)
TextLabel.Font = Enum.Font.SpecialElite
TextLabel.Text = "   .gg/Nmrsw2Hub"
TextLabel.TextColor3 = Color3.fromRGB(247, 72, 119)
TextLabel.TextSize = 100.000
TextLabel.TextStrokeTransparency = 0.000
wait(4)
game.CoreGui:FindFirstChild("ScreenGui"):Destroy()

wait(1)

local Watermark = Instance.new("ScreenGui")
local ImageLabel = Instance.new("ImageLabel")
local name = Instance.new("TextLabel")
local fps = Instance.new("TextLabel")
local cb = Instance.new("TextLabel")

Watermark.Name = "Watermark"
Watermark.Parent = game.CoreGui

ImageLabel.Parent = Watermark
ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageLabel.BorderSizePixel = 0
ImageLabel.Position = UDim2.new(0.07, 0, -0.0255202732, 0)
ImageLabel.Size = UDim2.new(0, 350, 0, 25)
ImageLabel.Image = "http://www.roblox.com/asset/?id=6837981571"

name.Name = "name"
name.Parent = ImageLabel
name.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
name.BackgroundTransparency = 1.000
name.Position = UDim2.new(0.0398406386, 0, -0.199999794, 0)
name.Size = UDim2.new(0, 71, 0, 35)
name.Font = Enum.Font.Code
name.Text = "    User : Retract "
name.TextColor3 = Color3.fromRGB(255, 255, 255)
name.TextSize = 14.000

fps.Name = "fps"
fps.Parent = ImageLabel
fps.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
fps.BackgroundTransparency = 1.000
fps.Position = UDim2.new(0.289929748, 0, 0.0799999982, 0)
fps.Size = UDim2.new(0, 150, 0, 20)
fps.Font = Enum.Font.Code
fps.Text =  "60 fps"
fps.TextColor3 = Color3.fromRGB(255, 255, 255)
fps.TextSize = 14.000

cb.Name = "cb"
cb.Parent = ImageLabel
cb.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
cb.BackgroundTransparency = 1.000
cb.Position = UDim2.new(0.70826441, 22, 0, 0)
cb.Size = UDim2.new(0, 6, 0, 22)
cb.Font = Enum.Font.Code
cb.Text = "     private cheat   "
cb.TextColor3 = Color3.fromRGB(255, 255, 255)
cb.TextSize = 14.000

local function GWWZ_fake_script() -- fps.LocalScript 
    local script = Instance.new('LocalScript', fps)

    local FPS = 0
    
    local Tiempo = tick()
    
    spawn(function()
        while game:GetService("RunService").RenderStepped:wait() do
            local Transcurrido = math.abs(Tiempo-tick())
            Tiempo = tick()
            FPS = math.floor(1/Transcurrido)
        end
    end)
    
    while wait(0.5) do
        script.Parent.Text = tostring(FPS) .. " fps"
    end
end
coroutine.wrap(GWWZ_fake_script)()

local function ZTKOG_fake_script() -- ImageLabel.LocalScript 
    local script = Instance.new('LocalScript', ImageLabel)

    local UIS = game:GetService("UserInputService")
    function dragify(Frame)
        dragToggle = nil
        local dragSpeed = 0
        dragInput = nil
        dragStart = nil
        local dragPos = nil
        function updateInput(input)
            local Delta = input.Position - dragStart
            local Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + Delta.X, startPos.Y.Scale, startPos.Y.Offset + Delta.Y)
            game:GetService("TweenService"):Create(Frame, TweenInfo.new(0.25), {Position = Position}):Play()
        end
        Frame.InputBegan:Connect(function(input)
            if (input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch) and UIS:GetFocusedTextBox() == nil then
                dragToggle = true
                dragStart = input.Position
                startPos = Frame.Position
                input.Changed:Connect(function()
                    if input.UserInputState == Enum.UserInputState.End then
                        dragToggle = false
                    end
                end)
            end
        end)
        Frame.InputChanged:Connect(function(input)
            if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
                dragInput = input
            end
        end)
        game:GetService("UserInputService").InputChanged:Connect(function(input)
            if input == dragInput and dragToggle then
                updateInput(input)
            end
        end)
    end
    
    dragify(script.Parent)
end
coroutine.wrap(ZTKOG_fake_script)()

wait(0.1)
local DiscordLib = loadstring(game:HttpGet"https://raw.githubusercontent.com/dawid-scripts/UI-Libs/main/discord%20lib.txt")()

local win = DiscordLib:Window(".gg/Nmrsw2Hub")

local serv = win:Server("Farm", "http://www.roblox.com/asset/?id=6031075938")

local btns = serv:Channel("Main")

btns:Label("Tip: Freeze first then start autofarm + minimize script")
btns:Label("Make sure that you are on fullscreen and close the chat")

btns:Button("Autofarm (F : keyblind)", function()

    local Players = game:GetService('Players')
    local CoreGui = game:GetService('StarterGui')
    local ReplicatedStorage = game:GetService('ReplicatedStorage')
    local ContextActionService = game:GetService('ContextActionService')
    local VirtualInputManager = game:GetService('VirtualInputManager')
    
    local LocalPlayer = Players.LocalPlayer
    
    local Enabled = false
    local Rod = false
    local Casted = false
    local Progress = false
    local Finished = false
    
    local Keybind = Enum.KeyCode.F
    
    function ShowNotification(String)
        CoreGui:SetCore('SendNotification', {
            Title = 'Notification',
            Text = String,
            Duration = 1
        })
    end
    
    function ToggleFarm(Name, State, Input)
        if State == Enum.UserInputState.Begin then
            Enabled = not Enabled
    
            print("Farm")
            
            if not Enabled then
                Finished = false
                Progress = false
                
            end
            
            ShowNotification(`Status: {Enabled}`)
        end
    end
    
    LocalPlayer.Character.ChildAdded:Connect(function(Child)
        if Child:IsA('Tool') and Child.Name:lower():find('rod') then
            Rod = Child
        end
    end)
    
    LocalPlayer.Character.ChildRemoved:Connect(function(Child)
        if Child == Rod then
            Enabled = false
            Finished = false
            Progress = false
            Rod = nil
        end
    end)
    
    LocalPlayer.PlayerGui.DescendantAdded:Connect(function(Descendant)
        if Descendant.Name == 'button' and Descendant.Parent.Name == 'safezone' then
            task.wait(0.01)
            local ButtonPosition, ButtonSize = Descendant.AbsolutePosition, Descendant.AbsoluteSize
            VirtualInputManager:SendMouseButtonEvent(ButtonPosition.X + (ButtonSize.X / 2), ButtonPosition.Y + (ButtonSize.Y / 2), Enum.UserInputType.MouseButton1.Value, true, LocalPlayer.PlayerGui, 1)
            VirtualInputManager:SendMouseButtonEvent(ButtonPosition.X + (ButtonSize.X / 2), ButtonPosition.Y + (ButtonSize.Y / 2), Enum.UserInputType.MouseButton1.Value, false, LocalPlayer.PlayerGui, 1)
        elseif Descendant.Name == 'playerbar' and Descendant.Parent.Name == 'bar' then
            Finished = true
            Descendant:GetPropertyChangedSignal('Position'):Wait()
            ReplicatedStorage.events.reelfinished:FireServer(100, true)
        end
    end)
    
    LocalPlayer.PlayerGui.DescendantRemoving:Connect(function(Descendant)
        if Descendant.Name == 'reel' then
            Finished = false
            Progress = false
        end
    end)
    
    coroutine.wrap(function()
        while true do
            if Enabled and not Progress then
                if Rod then
                    Progress = true
                    task.wait(0.5)
                    Rod.events.cast:FireServer(100.5)
                end
            end
        
            task.wait()
        end
    end)()
    
    local NewRod = LocalPlayer.Character:FindFirstChildWhichIsA('Tool')
    
    if NewRod and NewRod.Name:lower():find('rod') then
        Rod = NewRod
    end
    
    ContextActionService:BindAction('ToggleFarm', ToggleFarm, false, Keybind)
    ShowNotification(`Press '{Keybind.Name}' to enable/disable`)
DiscordLib:Notification("Notification", "F to start fishing", "Okay!")
end)

btns:Seperator()

btns:Button("Freeze (K : keyblind)", function()

    local Players = game:GetService("Players")
    local RunService = game:GetService("RunService")
    local UIS = game:GetService("UserInputService")
    
    local LocalPlayer = Players.LocalPlayer
    local Character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
    local HumanoidRootPart = Character:WaitForChild("HumanoidRootPart")
    
    local isFrozen = false
    local freezeConnection
    
    -- Store the original CFrame (position and orientation)
    local lastCFrame
    
    -- Function to freeze the player's CFrame
    local function freezePlayer()
        lastCFrame = HumanoidRootPart.CFrame -- Capture the last CFrame
        
        -- Start a loop to keep resetting the player's CFrame
        freezeConnection = RunService.Heartbeat:Connect(function()
            if isFrozen then
                -- Lock the player's CFrame (position and orientation) every Heartbeat frame
                HumanoidRootPart.CFrame = lastCFrame
                -- Reset the velocity to ensure no unintended movement
                HumanoidRootPart.Velocity = Vector3.new(0, 0, 0)
            end
        end)
    end
    
    -- Function to unfreeze the player
    local function unfreezePlayer()
        if freezeConnection then
            freezeConnection:Disconnect() -- Stop freezing the CFrame
            freezeConnection = nil
        end
    end
    
    -- Toggle freezing/unfreezing
    local function toggleFreeze()
        isFrozen = not isFrozen
        
        if isFrozen then
            lastCFrame = HumanoidRootPart.CFrame -- Set the last CFrame when freezing
            freezePlayer() -- Start freezing
        else
            unfreezePlayer() -- Stop freezing
        end
    end
    
    -- Example usage: Press 'K' to toggle freeze/unfreeze
    UIS.InputBegan:Connect(function(input)
        if input.KeyCode == Enum.KeyCode.K then
            toggleFreeze()
        end
    end)
    
DiscordLib:Notification("Notification", "K to freeze yourself", "Okay!")
end)

btns:Seperator()

btns:Button("Press to Farm (for mobile)", function()
local UserInputService = game:GetService("UserInputService")

UserInputService.InputBegan:Connect(function(input, gameProcessed)
    if not gameProcessed and input.KeyCode == Enum.KeyCode.F then
        -- Trigger whatever action you want to associate with pressing F
        print("Start Autofarm!") -- Replace with your desired action
    end
end)

end)


local btns2 = serv:Channel("Misc")

btns2:Button("Inf Oxygen", function()
local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer
local Workspace = game:GetService("Workspace")

-- Function to disable the LoadScript for the LocalPlayer
local function disableLoadScript()
    local oxygenScript = Workspace.LocalPlayer.client:FindFirstChild("oxygen")
    
    if oxygenScript and oxygenScript:IsA("Script") then
        oxygenScript.Enabled = false -- Disable the script
        print("Oxygen script disabled.")
    else
        print("Oxygen script not found or is not a script.")
    end
end

-- Call the function to disable the LoadScript
disableLoadScript()
end)

btns2:Seperator()

btns2:Button("Sell All", function()
    workspace:WaitForChild("world"):WaitForChild("npcs"):WaitForChild("Marc Merchant"):WaitForChild("merchant"):WaitForChild("sellall"):InvokeServer()
end)

btns2:Seperator()

btns2:Button("Sell Held Item", function()
    workspace:WaitForChild("world"):WaitForChild("npcs"):WaitForChild("Marc Merchant"):WaitForChild("merchant"):WaitForChild("sell"):InvokeServer()
end)

btns2:Seperator()

btns2:Button("Appraise Held Item", function()
    workspace:WaitForChild("world"):WaitForChild("npcs"):WaitForChild("Appraiser"):WaitForChild("appraiser"):WaitForChild("appraise"):InvokeServer()
end)

btns2:Seperator()

btns2:Button("infiniteyield", function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
end)

btns2:Seperator()

btns2:Button("NoCDGrabCandy (event)", function()
    for i,v in ipairs(game:GetService("Workspace"):GetDescendants()) do
        if v.ClassName == "ProximityPrompt" then
            v.HoldDuration = 0
        end
    end
end)



local btns3 = serv:Channel("Teleport")

btns3:Button("Frightful Pool", function()
    --[[ 
    WARNING: Heads up! This script has not been verified by ScriptBlox. Use at your own risk! 
]]

local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer
local Workspace = game:GetService("Workspace")

-- Target CFrame with Y offset
local targetPart = Workspace.zones.fishing.FischFright24

if targetPart then
    -- Get the current position of the target part and add 100 to the Y coordinate
    local newPosition = targetPart.Position + Vector3.new(0, 100, 0)

    -- Teleport the LocalPlayer's character to the new position
    local character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
    character:SetPrimaryPartCFrame(CFrame.new(newPosition))
else
    print("Not Spawn Yet.")
end

end)

btns3:Seperator()

btns3:Button("Moosewood", function()
local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(386, 135, 252))
end)

btns3:Button("Statue", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(73, 142, -1028))
end)

btns3:Button("Lava", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(-1889, 168, 329))
end)

btns3:Button("Arch", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(999, 131, -1237))
end)

btns3:Button("spike", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(-1255, 138, 1554))
end)

btns3:Button("Birch", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(1742, 142, -2502))
end)

btns3:Button("Mushgrove", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(2501, 131, -721))
end)

btns3:Button("Keepers", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(1296, -805, -299))
end)

btns3:Button("Executive", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(-30, -247, 199))
end)

btns3:Button("Swamp", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(2501, 131, -721))
end)

btns3:Button("Snowcap", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(2649, 142, 2521))
end)

btns3:Button("Wilson", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(2939, 281, 2567))
end)

btns3:Button("Roslit", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(-1477, 134, 672))
end)

btns3:Button("Vertigo", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(-112, -515, 1040))
end)

btns3:Button("Sunstone", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(-933, 132, -1120))
end)

btns3:Button("Terrapin", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(-144, 145, 1910))
end)

btns3:Button("Deep Ocean (safeplace)", function()
    local Players = game:GetService("Players")
Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(-508, -62, -7688))
DiscordLib:Notification("Notification", "Face at the water to cast", "Okay!")
end)

local btns4 = serv:Channel("Credit")

btns4:Label("Script developed by Tuckky นมร. & Teng1")
btns4:Label("We believe in creating experiences that empower and inspire.")
btns4:Label("Every line of code is infused with love.")
btns4:Label("Thank you for being a part of our journey!")
