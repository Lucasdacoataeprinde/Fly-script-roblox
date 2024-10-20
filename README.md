loadstring("local player = game.Players.LocalPlayer; local character = player.Character; local humanoid = character:WaitForChild('Humanoid'); local flightEnabled = false; local flightSpeed = 10;

local function toggleFlight() 
    if flightEnabled then 
        flightEnabled = false 
    else 
        flightEnabled = true 
    end 
end 

local function fly() 
    if flightEnabled then 
        local pos = character.HumanoidRootPart.Position 
        character.HumanoidRootPart.Velocity = Vector3.new(0, flightSpeed, 0) 
        wait(0.1) 
        character.HumanoidRootPart.Position = pos 
    end 
end 

-- Hub Script

loadstring("local player = game.Players.LocalPlayer; local character = player.Character; local humanoid = character:WaitForChild('Humanoid'); local hub = Instance.new('ScreenGui'); hub.Name = 'FlightHub'; 

local flyButton = Instance.new('TextButton'); flyButton.Text = 'Fly'; flyButton.BackgroundColor3 = Color3.new(0, 1, 0); flyButton.Position = UDim2.new(0, 0, 0, 0); flyButton.Size = UDim2.new(0, 100, 0, 50); flyButton.Parent = hub; 

flyButton.MouseButton1Click:Connect(toggleFlight) 

hub.Parent = game.Players.LocalPlayer.PlayerGui")
