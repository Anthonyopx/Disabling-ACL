local Players = game:GetService("Players")

-- When a player joins, check their chat
Players.PlayerAdded:Connect(function(player)
    player.Chatted:Connect(function(message)
        -- If someone tries to use chat logging, block the message
        if message:lower():find("chatlog") or message:lower():find("logger") then
            warn("Blocked possible chat logger from: " .. player.Name)
        end
    end)
end)
if string.find(message, "spy") or string.find(message, "chatlog") then
