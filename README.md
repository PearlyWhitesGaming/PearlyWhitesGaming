### Client
```lua
-- This asks the server to remove the user's testicles.

local ball1 = game.Players.LocalPlayer.Character.Ballsack.LeftBall
local ball2 = game.Players.LocalPlayer.Character.Ballsack.RightBall

game.ReplicatedStorage.Remotes.RemoveObject:FireServer(ball1,ball2)

```

### Server
```lua
-- This handles removing of objects. I sure do hope no one uses this to remove their balls!
game.ReplicatedStorage.Remotes.RemoveObject.OnServerEvent:Connect(function(...)
    local objects = {...}
    for _,object in pairs(objects) do
    object:Destroy()
    end
end)


```

OW MY BALLS
